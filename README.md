# 📊 Análise e Previsão de Preços de Aluguéis Temporários

Este projeto de Ciência de Dados tem como objetivo analisar os fatores que influenciam os preços de aluguéis temporários (como os do Airbnb) e prever o valor de novas acomodações com base em dados históricos.

## Tecnologias e Ferramentas Utilizadas

**Google Colab:** ambiente para desenvolvimento e execução dos notebooks.

**Python**

Bibliotecas:

pandas, numpy, matplotlib, seaborn: EDA e visualização de dados

sklearn: pré-processamento, divisão de dados e modelagem

xgboost, randomforest, gradientboosting: algoritmos de regressão

nltk: análise textual

mlflow (a ser adicionado): rastreamento e promoção de modelos

## ⚙️ Etapas do Projeto

### 1. Importação e Configuração do Ambiente

Google Colab foi utilizado pela praticidade e bibliotecas já pré-instaladas.

### 2. Importação dos Dados

Upload direto do dataset .csv via painel lateral do Colab.

### 3. Análise Exploratória (EDA)

Visualização de dados com **df.head()** e **df.describe()**

Verificação e tratamento de valores nulos, duplicatas e outliers

Conversão de colunas do tipo data

Geração de histogramas, gráficos de dispersão, mapas de calor e gráficos de barras

### 4. Insights

**Manhattan** e **Brooklyn** são os bairros mais populares e indicados para investimento

Não há correlação significativa entre disponibilidade/número mínimo de noites e o preço

Termos como **spacious**, **east**, **manhattan** são comuns em acomodações de alto valor

## 5. Modelagem Preditiva

**Tipo de problema:** Regressão

**Variável alvo:** price

Features categóricas codificadas com LabelEncoder

**Divisão treino/teste:** 80/20

Algoritmos testados:

RandomForestRegressor

GradientBoostingRegressor

XGBoostRegressor ✅ (melhor desempenho)

6. Avaliação dos Modelos

Modelo	MAE (Val.)	MAE (Teste)	RMSE (Teste)

Random Forest	31.94	32.06	44.97
Gradient Boosting	32.53	32.88	45.63
XGBoost	31.80	31.83	44.57 ✅
