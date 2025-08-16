# 📉 Projeto Data Science: Evasão de Clientes - TelecomX

Este projeto tem como objetivo analisar os dados de clientes da TelecomX para identificar padrões e fatores que levam à evasão (churn) de clientes. A análise exploratória de dados (EDA) e a engenharia de variáveis foram realizadas para obter insights sobre o comportamento dos clientes.

## 📦 Importação de Bibliotecas

Foram utilizadas as bibliotecas pandas para manipulação de dados, matplotlib e seaborn para visualização, e json para carregar os dados.

## 📥 Carregamento de Dados

Os dados foram carregados a partir de um arquivo JSON (`TelecomX_Data.json`) e normalizados em um DataFrame pandas.

## 🧼 Limpeza de Dados

Valores vazios foram substituídos por `pd.NA` e a coluna `account_Charges_Total` foi convertida para tipo numérico, tratando possíveis erros com `errors='coerce'`. Linhas com valores diferentes de 'Yes' ou 'No' na coluna 'Churn' foram removidas.

## 🧪 Engenharia de Variáveis

Novas variáveis foram criadas para facilitar a análise:
- `Churn_flag`: Variável binária (1 para 'Yes', 0 para 'No') representando a evasão.
- `SeniorCitizen`: Categoriza clientes como 'Senior' ou 'Adult'.
- `tenure_years`: Converte o tempo de contrato de meses para anos.

## 📊 EDA - Análise Exploratória de Dados

Foram gerados gráficos para visualizar a distribuição do churn e a relação entre churn e outras variáveis, como tipo de contrato, forma de pagamento e gasto mensal.

## 🔥 Correlação

Um heatmap foi gerado para visualizar a correlação entre as variáveis numéricas importantes para a análise de churn.

## 🧾 Conclusões

- Contratos **mensais** têm maior propensão ao cancelamento.
- Clientes **recentes (menos de 1 ano)** representam boa parte das evasões.
- Forma de pagamento **Cheque eletrônico** está relacionada à evasão.
- Falta de serviços adicionais como **Segurança Online** e **Suporte Técnico** é frequente entre clientes que saem.

## 📌 Recomendações

- Estimular planos **anuais ou bianuais**.
- Programas de **retenção para novos clientes**.
- Incentivar outros métodos de pagamento.
- Oferecer **pacotes combinados** com serviços adicionais.
