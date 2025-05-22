# Case_QA Project

## Introdução

O **Case_QA Project** tem como objetivo analisar e modelar dados de compartilhamento de bicicletas. Este projeto explora o comportamento dos aluguéis através de análises visuais e modelos preditivos, possibilitando a identificação de padrões sazonais, tendências e variáveis-chave que influenciam o uso das bicicletas.

## Descrição dos Dados

O dataset utilizado contém informações como:
- Data e hora dos aluguéis
- Temperatura, sensação térmica, umidade e velocidade do vento
- Número de usuários casuais e registrados
- Indicadores de feriados, dias úteis e condições climáticas

Os dados são extraídos de um arquivo Excel (`Capital_share_bike__1___1_.xlsx`), localizado na pasta `src/table`.

## Análise Exploratória (EDA)

No notebook **eda.ipynb**, foram realizadas as seguintes etapas:
- **Carregamento e pré-processamento:** Leitura do dataset e criação de novas colunas (ano, mês, dia, hora, dia da semana, estação, etc.);
- **Visualização dos dados:** Criação de gráficos como pairplots, heatmaps e gráficos de linha para identificar correlações e padrões temporais;
- **Verificação da distribuição temporal:** Análise dos registros por dia, identificando lacunas e padrões de uso ao longo do tempo;
- **Gráficos polares:** Exploração dos padrões de uso por hora e por período (dias úteis x não úteis) para identificar horários "nobres".

## Modelagem Preditiva

No notebook **modeling.ipynb**, a modelagem preditiva é realizada com as seguintes abordagens:
- **Regressão por Mínimos Quadrados Parciais (PLS):** Para avaliar a contribuição de cada variável no modelo preditivo;
- **XGBoost:** Utilizado para prever o número de aluguéis e avaliar o desempenho do modelo através de métricas como R², RMSE, MAE, WMAPE e Bias;
- **Visualização dos resultados:** Gráficos de barras que apresentam os coeficientes da regressão PLS são gerados, complementados com as métricas de desempenho do modelo.

## Requisitos

O projeto utiliza as seguintes bibliotecas:
- pandas
- numpy
- matplotlib
- seaborn
- plotly
- july
- xgboost
- scikit-learn

Consulte o arquivo `requirements.txt` para as versões específicas.

## Como Executar

1. **Clone o repositório:**
   ```bash
   git clone https://github.com/rodrili/case_qa.git
   cd case_qa
   ```
2. **Instale as dependências:**
   ```bash
   pip install -r requirements.txt
   ```
3. **Abra os notebooks:**
   Utilize um ambiente que suporte Jupyter Notebooks (VSCode, JupyterLab, etc.) para abrir e executar os notebooks `eda.ipynb` e `modeling.ipynb`.

## Conclusão

O **Case_QA Project** fornece uma análise completa dos dados de compartilhamento de bicicletas, desde a exploração inicial até a modelagem preditiva, permitindo uma melhor compreensão dos fatores que influenciam o uso das bicicletas e oferecendo subsídios para decisões estratégicas na mobilidade urbana.
