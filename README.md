# MVP - Previsão de Preços de Casas (Boston Housing Dataset)

Este projeto tem como objetivo a construção de um modelo de Ciência de Dados para prever o preço das casas com base em atributos como o número de quartos, área, localização, entre outros. O dataset utilizado é o **Boston Housing Dataset**, que contém informações sobre diferentes características das casas em Boston, EUA, e seus respectivos preços.

## Objetivo

O objetivo deste projeto é construir um modelo de regressão para prever os preços das casas com base em características como:

- Número de quartos
- Tamanho da casa
- Localização
- Proximidade de áreas de recreação e escolas
- Nível de poluição
- E outros fatores

O modelo construído pode ser utilizado para estimar o valor de casas em Boston, ajudando em decisões relacionadas à compra e venda de imóveis.

## Descrição do Problema

### Problema

A previsão precisa dos preços de casas é importante para diversos setores, como compra e venda de imóveis, análise de mercado e planejamento urbano. O modelo desenvolvido visa prever o preço de casas com base em características específicas.

### Hipóteses

1. A relação entre as características das casas e seus preços pode ser modelada utilizando técnicas de regressão.
2. Algumas variáveis, como o número de quartos e o nível de poluição, têm um impacto significativo no preço das casas.

### Restrições

- O dataset utilizado é um conjunto histórico de dados de casas em Boston, que pode não refletir as condições atuais do mercado imobiliário.
- O modelo pode ter limitações ao generalizar para outras regiões ou cidades.

### Dataset

O dataset utilizado é o **Boston Housing Dataset**, que contém 506 amostras e 13 variáveis preditoras. A variável alvo (y) é o preço das casas (`MEDV`).

Abaixo estão as variáveis presentes no dataset:

- **CRIM**: Taxa de criminalidade per capita
- **ZN**: Proporção de áreas residenciais com grande parcela de terrenos para construção
- **INDUS**: Proporção de acres de negócios não varejistas por cidade
- **CHAS**: Variável indicadora de proximidade ao rio Charles (1 se a casa está ao lado do rio, 0 caso contrário)
- **NOX**: Concentração de óxidos de nitrogênio
- **RM**: Número médio de quartos por residência
- **AGE**: Proporção de casas construídas antes de 1940
- **DIS**: Distância ponderada para centros de emprego em Boston
- **RAD**: Índice de acessibilidade à rodovias radiais
- **TAX**: Taxa sobre propriedades de valor mais alto
- **PTRATIO**: Razão aluno-professor
- **B**: Proporção de moradores de origem africana
- **LSTAT**: Percentual de pessoas de classe baixa na população

## Preparação de Dados

- O dataset foi carregado e tratado para garantir que não houvesse valores nulos.
- As variáveis foram normalizadas para garantir que todas estivessem na mesma escala.
- Utilizou-se **SelectKBest** para realizar a seleção das 10 melhores variáveis preditoras com base na correlação estatística.

## Modelagem e Treinamento

Foram treinados dois modelos de regressão para prever o preço das casas:

1. **Regressão Linear**: Um modelo simples, de fácil interpretação, que serve como baseline.
2. **Random Forest**: Um modelo mais complexo, capaz de capturar relações não-lineares entre as variáveis, e por isso, mais robusto.

### Resultados dos Modelos

- **Regressão Linear**:
  - **MSE**: 27.22
  - **R²**: 0.63
  - A regressão linear mostrou-se simples, mas com limitações para capturar relações complexas nos dados.
  
- **Random Forest**:
  - **MSE**: 9.62
  - **R²**: 0.87
  - O modelo Random Forest apresentou um desempenho superior, com previsões mais precisas e robustas.

### Gráficos

- **Valores Reais vs Preditos**:
  - O gráfico mostra a comparação entre os valores reais dos preços das casas e as previsões feitas pelos modelos de Regressão Linear e Random Forest.
  
- **Mapa de Correlação**:
  - O gráfico de correlação ajuda a entender como as variáveis do dataset se relacionam entre si.

## Conclusão

- O modelo **Random Forest** se mostrou o mais eficaz para prever os preços das casas, com um desempenho significativamente melhor que o modelo de **Regressão Linear**.
- O modelo é capaz de capturar padrões complexos nos dados e fornecer estimativas mais precisas para os preços das casas.
- Variáveis como o **número de quartos** e o **nível de poluição** têm um impacto importante no preço das casas.


## Bibliotecas Utilizadas

- `warnings`
- `pandas`
- `numpy`
- `matplotlib.pyplot`
- `seaborn`
- `sklearn.model_selection.train_test_split`
- `sklearn.model_selection.cross_val_score`
- `sklearn.preprocessing.StandardScaler`
- `sklearn.feature_selection.SelectKBest`
- `sklearn.ensemble.RandomForestRegressor`
- `sklearn.linear_model.LinearRegression`
- `sklearn.metrics.mean_squared_error`
- `sklearn.metrics.r2_score`
- `sklearn.model_selection.GridSearchCV`


   
