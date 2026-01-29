# 📊 Análise da Evasão de Clientes



Este projeto tem como objetivo trabalhar com um conjunto de dados gerado artificialmente sobre o "churn" de clientes de um determinado banco fictício. Em suma, tal banco está tendo dificuldade em manter os clientes e como sabemos, e por isso é necessário fazer uma análise detalhada para entender o que está acontecendo e influenciando para termos este problema.





## 🛠️ Composição dos Dados (Data Dictionary)



O dataset utilizado contém informações históricas de 10.000 clientes. Abaixo, a descrição detalhada de cada variável e sua relevância para a análise:



### 🆔 Dados de Identificação

- **RowNumber:** Índice numérico das linhas. Não possui valor analítico e foi desconsiderado na modelagem.

- **CustomerId:** Identificador único do cliente. Essencial para contagens distintas (`COUNTDISTINCT`) e cálculo do total de clientes.

- **Surname:** Sobrenome do cliente. Utilizado apenas para identificação, sem impacto direto na probabilidade de evasão.



### 👥 Perfil Demográfico

- **Geography:** País de residência do cliente (França, Alemanha, Espanha). Variável chave para identificar padrões regionais de evasão.

- **Gender:** Gênero do cliente. Importante para analisar se existe disparidade na taxa de saída entre homens e mulheres.

- **Age:** Idade do cliente. Historicamente, clientes mais velhos tendem a ter maior estabilidade e menor probabilidade de churn.



### 🏦 Relacionamento com o Banco

- **Tenure (Tempo de Permanência):** Quantos anos o cliente está no banco. Clientes com maior *tenure* tendem a ser mais leais.

- **NumOfProducts (Número de Produtos):** Quantidade de serviços contratados (Ex: Conta, Poupança, Seguro).

&nbsp;   * *Insight:* Geralmente, mais produtos indicam fidelidade, mas um número excessivo (3 ou 4) pode indicar venda forçada, gerando insatisfação e saída.

- **IsActiveMember (Membro Ativo):** Indicador binário (1 = Sim, 0 = Não) de movimentação ou interação frequente. Clientes ativos apresentam menor risco de saída.



### 💰 Saúde Financeira

- **CreditScore:** Pontuação de crédito (300-850) baseada no histórico financeiro. Clientes com scores mais altos (acima de 700) são considerados mais estáveis e menos propensos a sair.

- **Balance (Saldo Bancário):** Valor disponível na conta. Clientes com saldos elevados são ativos críticos para o banco, e sua perda representa um impacto financeiro maior (High Net Worth Churn).

- **EstimatedSalary:** Estimativa da renda anual. Ajuda a segmentar o comportamento de churn entre diferentes faixas de renda.



### 💳 Cartão de Crédito

- **HasCrCard:** Indica se o cliente possui cartão de crédito (1 = Sim, 0 = Não). A posse do cartão pode atuar como um fator de retenção (Lock-in).

- **Card Type:** Categoria do cartão (Silver, Gold, Diamond, Platinum).

- **Points Earned:** Pontos acumulados no programa de fidelidade. Clientes com muitos pontos tendem a pensar duas vezes antes de cancelar para não perder os benefícios.



### 🎯 Métricas Alvo e Qualidade (KPIs)

- **Exited (Churn):** A variável alvo (Target).

&nbsp;   - `0`: Cliente permaneceu.

&nbsp;   - `1`: Cliente saiu (Churn).

- **Complain (Reclamação):** Se o cliente registrou reclamação recente (1 = Sim). Esta variável provou ser o maior preditor de saída nesta análise.

- **Satisfaction Score:** Nota dada pelo cliente (1 a 5) para a resolução da reclamação. Avalia a eficácia do suporte na retenção de clientes insatisfeitos.



---



## 💼 O Problema de Negócio



O banco está enfrentando uma taxa de cancelamento (Churn) significativa. A diretoria precisa entender:

1.  **Impacto Financeiro:** Estamos perdendo clientes de baixo ou alto valor?

2.  **Perfil de Risco:** Existe um padrão demográfico (idade, gênero, região) nos clientes que saem?

3.  **Produtos:** O excesso ou falta de produtos bancários influencia a fidelidade?

4.  **Qualidade:** O suporte ao cliente está sendo eficaz na retenção de insatisfeitos?



---



## 🔍 Estrutura do Dashboard

O relatório foi dividido em 4 páginas estratégicas para guiar a narrativa dos dados:





### 1. Visão Geral (Overview)

Um panorama executivo da situação atual.

- **Principais KPIs:** Total de clientes, taxa de churn (20%) e taxa de perda financeira (24%)
- **Insight Crítico:** A perda financeira é superior a perda de clientes, o que nos indica a saída de correntistas com saldo acima da média, ou seja, um alto patrimônio. Além disso, vemos que existe uma relação direta entre a taxa de saída e o número de produtos, o que nos indica que quanto mais produtos se tentam vender aos clientes maior se torna a probabilidade deles deixarem o banco.



### 2. Análise Demográfica

Identificação de nichos de risco.

- **Perfil Identificado:** A maior incidência de evasão ocorre em **Mulheres**, na faixa de **40 a 50 anos**, residentes na **Alemanha**. Além disso, a maior parte das pessoas que saem são mais velhas, o que corrobora com a saída de clientes com um maior potencial aquisito.

- Visualização através de Mapas e Gráficos de Distribuição Etária.



### 3. Saúde Financeira e Produtos

Correlação entre a posse de produtos, score de crédito e saldo bancário.

- **Problema do Produto:** Identificou-se que clientes com **3 ou 4 produtos** possuem uma taxa de evasão de quase 100%, sugerindo falhas estruturais nesses pacotes ou vendas forçadas.

- **Renda vs. Evasão:** Clientes com saldos mais altos tendem a sair mais, confirmando o risco de perda de capital.

* **Clientes VIP:** Temos a saída de clientes importantes ao observar que aqueles com os cartões mais caros como Diamond e Platinum também apresentam uma taxa de evasão maior. Esse é um problema crítico nos mostrando que os benefícios desses cartões não estão fidelizando os clientes.



### 4. Atendimento ao Cliente

Análise da eficácia do suporte.

- **Correlação Alarmante:** 99,8% dos clientes que saíram realizaram uma reclamação prévia.

- **Ineficácia da Resolução:** A análise mostrou que mesmo clientes que avaliaram bem o atendimento acabaram saindo, indicando que a resolução do problema não está sendo efetiva para a retenção.



---



## 🛠️ Tecnologias e Técnicas Utilizadas

- **Power BI Desktop:** Construção do Dashboard e Storytelling.

- **DAX (Data Analysis Expressions):** Criação de medidas para análises comparativas.

&nbsp;   - Funções utilizadas: `CALCULATE`, `DIVIDE`, `COUNTROWS`, `ALL`, entre outras.

- **Modelagem de Dados:** Estruturação para garantir performance e integridade das relações.

- **Power Query:** Limpeza e tratamento dos dados brutos (ETL).















