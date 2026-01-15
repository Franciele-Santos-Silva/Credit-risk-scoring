# Credit Risk Scoring

Sistema de Machine Learning para previsão de score de crédito de clientes.

## Descrição do Projeto

Este projeto utiliza algoritmos de aprendizado de máquina para classificar o risco de crédito dos clientes em três categorias:

- **Good** (Bom) - Cliente com baixo risco de crédito
- **Standard** (Standard) - Cliente com risco médio de crédito  
- **Poor** (Ruim) - Cliente com alto risco de crédito

## Tecnologias Utilizadas

- **Python** - Linguagem de programação
- **Pandas** - Manipulação e análise de dados
- **Scikit-learn** - Machine Learning
  - RandomForestClassifier
  - KNeighborsClassifier
  - LabelEncoder
  - train_test_split
  - accuracy_score
- **Jupyter Notebook** - Ambiente de desenvolvimento

## Metodologia

### 1. Pré-processamento de Dados
- Conversão de variáveis categóricas para numéricas usando `LabelEncoder`
- Colunas categóricas convertidas:
  - `profissao`
  - `mix_credito`
  - `comportamento_pagamento`

### 2. Divisão dos Dados
- 70% para treino
- 30% para teste

### 3. Modelos Utilizados
- **RandomForestClassifier**: Ensemble de árvores de decisão
- **KNeighborsClassifier**: Classificador de vizinhos mais próximos

### 4. Avaliação
- Métrica: Acurácia (accuracy_score)
- Comparação entre os dois modelos para escolha do melhor

## Resultados

O modelo treinado pode ser usado para:
- Prever o score de crédito de novos clientes
- Auxiliar em decisões de aprovação de crédito
- Identificar clientes de alto risco

## Como Executar

1. Abra o arquivo `credit-risk-scoring.ipynb` em um ambiente Jupyter
2. Execute as células sequencialmente
3. O notebook carregará os dados, treinará os modelos e mostrará as previsões

## Observações

- O arquivo `novos_clientes.csv` contém clientes sem score_credito para os quais o modelo faz previsões
- As variáveis categóricas precisam ser transformadas antes de usar o modelo em novos dados
- O modelo RandomForest geralmente apresenta melhor desempenho para este tipo de problema
