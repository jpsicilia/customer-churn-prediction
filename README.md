# customer-churn-prediction
Projeto de Machine Learning para prever a taxa de cancelamento (churn) de clientes de uma empresa de telecomunicações

# Previsão de Churn de Clientes com Machine Learning

## 1. Objetivo do Projeto
O objetivo deste projeto é construir e avaliar múltiplos modelos de classificação para prever proativamente quais clientes têm uma alta probabilidade de cancelar seu serviço. O objetivo de negócio é maximizar a deteção desses clientes (recall) para permitir ações de retenção eficazes.

## 2. Dataset
Foi utilizado o dataset "Telco Customer Churn" do Kaggle, que contém informações demográficas, de conta e de serviços dos clientes.

## 3. Metodologia
O projeto seguiu um fluxo de trabalho completo de ciência de dados:
* **Análise Exploratória de Dados (EDA):** Para entender a estrutura e as relações nos dados.
* **Pré-processamento:** Limpeza de dados e construção de um Pipeline robusto com `ColumnTransformer` para padronizar variáveis numéricas e codificar variáveis categóricas (`OneHotEncoder`).
* **Modelagem:** Foram treinados e comparados 3 modelos:
    1. Regressão Logística (como linha de base)
    2. Random Forest
    3. XGBoost
* **Otimização:** Foi utilizado o `RandomizedSearchCV` para encontrar os melhores hiperparâmetros para os modelos avançados, otimizando para diferentes métricas (`recall` e `f1-score`).

## 4. Principais Resultados
O modelo final, um **XGBoost otimizado**, provou ser o mais eficaz para o objetivo de negócio, alcançando um **recall de 91%**. Isso significa que ele é capaz de identificar 9 de cada 10 clientes que realmente estão em risco de sair.

## 5. Tecnologias Utilizadas
* Python
* Pandas e NumPy
* Scikit-learn (Pipeline, ColumnTransformer, RandomizedSearchCV)
* XGBoost
* Matplotlib e Seaborn
