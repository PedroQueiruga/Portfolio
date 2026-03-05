# Quick Commerce: Análise de Performance e Eficiência Operacional

O Quick Commerce (ou Q-Commerce) representa a evolução do e-commerce tradicional, focando na entrega ultra-rápida (frequentemente em menos de uma hora) de produtos de conveniência, mantimentos e itens essenciais. Esse modelo tem suas origens nos sistemas de delivery de comida, mas adaptado para a entrega de outros tipos de produtos.

Este projeto tem como objetivo central realizar uma análise exploratória e estratégica sobre a eficiência operacional e o desempenho de vendas de diferentes players deste setor. Através de um dashboard interativo no Excel, buscamos identificar não apenas o market share das empresas, mas também gargalos logísticos e oportunidades de expansão geográfica, fornecendo subsídios para a tomada de decisão baseada em dados.

---

## 📝 Fonte dos dados

Os dados utilizados neste projeto são sintéticos, mas uma simulação realística do Q-Commerce. Eles foram extraídos da plataforma Kaggle e representam o cenário competitivo de empresas de entrega rápida, incluindo métricas de vendas, tempo de entrega, avaliações de clientes e segmentações geográficas.

* **Fonte original:** [Quick Commerce Dataset - Kaggle](https://www.kaggle.com/datasets/rohitgrewal/quick-commerce-dataset)

---

## Perguntas de Negócios
Ao longo do desenvolvimento do dashboard, refinamos nossa abordagem analítica. As seguintes perguntas guiaram a construção das nossas visualizações:

* **Qual é o volume total de vendas e pedidos no período?** (Respondida via KPIs de alta visibilidade).

* **Como está distribuído o Market Share entre as companhias?** (Respondida pelo gráfico de total de vendas por empresa).

* **Existe correlação entre o volume de pedidos e a eficiência da entrega?** (Respondida através da análise combinada de pedidos vs. tempo médio de entrega).

* **Quais cidades possuem o melhor desempenho financeiro?** (Respondida pelo gráfico Top 5 Cidades por Receita).

* **Qual é a satisfação média dos clientes por praça?** (Respondida via análise de rating consolidada).

* **Com base no desempenho atual, em quais cidades as empresas devem expandir?** (Respondida através do gráfico de comparação do potencial de mercado e a qualidade do serviço).

---
## Resultados

A análise dos dados de Q-commerce permitiu a extração de insights estratégicos que conectam eficiência operacional, satisfação do cliente e performance financeira. Abaixo é detalhado as conclusões extraídas das perguntas de negócios:

* Dominância de Mercado E Fidelização: A Swiggy Instamart consolidou-se como a líder em rendimento bruto, sustentada por uma alta avaliação média dos clientes. Observamos uma correlação clara entre a satisfação do cliente e o volume de vendas, confirmando que a fidelização é o principal motor de crescimento no seto: experiências de compra positivas impulsionam o LTV (Lifetime Value) do cliente. Empresas com baixo desempenho de vendas, apresentam, invariavelmente, notas de avaliação abaixo da média, sugerindo que o investimento em atendimento ao cliente é um pré-requisito para escalar o market share.

* Oportunidades em Lugares de Alta Receita: A análise por cidade, destacou polos vitais, como Gurgaon e Noida, que concentram o maior volume de receita. Identificamos um caso crítico em Noida: Apesar de ser uma das cidades mais lucrativas, sua avaliação média é inferior à outras metrópoles. Este gap sinaliza uma oportunidade imediata de incremento de lucro: a correção de falhas operacionais nesta praça pode elevar a satisfação, aumentar a recorrência e, consequentemente, maximizar a receita mensal em um mercado onde a demanda já está validada.

* Volume de mercado: O ecossistema analisado movimenta um volume bruto de R$ 523 milhões, evidenciando o alto impacto e a capilaridade deste modelo de negócio.

* O "Triângulo" Operacional (Tempo, Venda e Rating): Existe uma relação direta entre o tempo de entrega e a saúde financeira da operação. Companhias com tempos de entrega prolongados apresentam declínio tanto na quantidade de pedidos quanto na avaliação média. Embora algumas empresas consigam manter um volume relevante mesmo com tempos de entrega maiores, observamos que o ticket médio de seus pedidos tende a ser inferior, reforçando que a agilidade na logística é o que sustenta a venda de produtos com maior valor agregado.

* Estratégia de Expansão: Com base no desempenho, concluímos que o foco de expansão não deve ser puramente volumétrico, mas qualitativo. A Matriz de Quadrantes (Gráfico de potencial de mercado e qualidade de serviços) desenvolvida aponta que cidades com baixa nota de satisfação e alto volume de vendas são "alertas de risco" que demandam otimização logística antes de qualquer expansão massiva.