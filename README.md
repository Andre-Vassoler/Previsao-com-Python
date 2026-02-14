## 📊 Previsão de Score de Crédito com Machine Learning

Projeto de Machine Learning desenvolvido em Python para prever o score de crédito de novos clientes como GOOD (bom), STANDARD (médio) ou POOR (ruim), com base em dados históricos.

## 🧠 Desafio do Projeto

Simular um cenário empresarial onde precisamos criar um sistema capaz de analisar as informações de um cliente e prever a probabilidade dele ser um bom ou mau pagador.

A previsão é feita utilizando dados existentes (clientes.csv) para treinar a IA e depois aplicando o modelo em novos clientes (novos_clientes.csv).

## 📁 Estrutura do Projeto
📂 previsao-score-credito
- clientes.csv    (Base de dados para treinamento)
- novos_clientes.csv    (Base de dados para novas previsões)
- inicial.ipynb    (Notebook com todo o desenvolvimento)
- README.md    (Documentação do projeto)

## ⚙️ Passo a Passo do Projeto
🔹 Passo 1: Importar a Base de Dados

Utilizamos as bibliotecas:

- Pandas
- Scikit-learn

Leitura e análise inicial da base de clientes para entender os dados e possíveis valores nulos.

🔹 Passo 2: Tratamento e Preparação dos Dados

Como modelos de IA trabalham apenas com números, colunas categóricas (texto) foram convertidas utilizando LabelEncoder, como:

profissão

mix_credito

comportamento_pagamento

Além disso:

Variável alvo (y): score_credito

Variáveis de entrada (x): todas as colunas, exceto score_credito e id_cliente

Também foi realizada a divisão entre:

Dados de treino

Dados de teste (30%)

🔹 Passo 3: Criação dos Modelos de IA

Foram utilizados dois algoritmos de classificação:

Random Forest (Árvore de Decisão)

KNN (K-Nearest Neighbors)

Os modelos foram treinados com os dados de treino para aprender os padrões da base.

🔹 Passo 4: Avaliação e Escolha do Melhor Modelo

As previsões foram comparadas com os dados reais de teste utilizando a métrica accuracy_score.

Resultado:

O modelo Random Forest apresentou melhor desempenho, com aproximadamente 82% de acerto.

🔹 Passo 5: Previsão de Novos Clientes

Após escolher o melhor modelo (Árvore de Decisão), aplicamos o modelo na base novos_clientes.csv para prever o score de crédito.

Exemplo de saída:

Poor

Poor

Standard

## 🛠️ Tecnologias Utilizadas
- Python
- Pandas
- Scikit-learn
- Jupyter Notebook

## 🚀 Como Executar o Projeto

- Baixe os arquivos 
- Instale as dependências:

    pip install pandas scikit-learn notebook


## 🎯 Objetivo Final

Criar um modelo de Inteligência Artificial capaz de analisar dados de clientes e prever automaticamente seu score de crédito, auxiliando empresas na tomada de decisões financeiras e análise de risco.
