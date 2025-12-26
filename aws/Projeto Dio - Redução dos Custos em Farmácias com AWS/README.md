# RELATÓRIO DE IMPLEMENTAÇÃO DE SERVIÇOS AWS

Data: 26/12/2025
Empresa: Abstergo Industries 
Responsável: Pedro Gonçalves

---

## Introdução
Este relatório apresenta o processo de implementação de ferramentas na empresa Abstergo Industries, realizado por Pedro Gonçalves. O objetivo do projeto foi elencar 3 serviços AWS, com a finalidade de realizar diminuição de custos imediatos.

---

## Descrição do Projeto
O projeto de implementação de ferramentas foi dividido em 3 etapas, cada uma com seus objetivos específicos. A seguir, serão descritas as etapas do projeto:

Etapa 1: Eficiência Computacional

- Amazon EC2 com Auto Scaling
- Essa ferramenta vai fornecer uma capacidade de computação que aumenta ou diminui automaticamente de acordo com a demanda do sistema de pedidos. Ela vai ter como objetivo ajudar no processamento de pedidos que são realizados através do uso de servidores virtuais.
- Implementaremos o sistema principal da distribuidora em instâncias EC2. Configuraremos um Auto Scaling Group com um tamanho mínimo para períodos de baixa atividade e um tamanho desejado para os horários de pico de vendas. Essa abordagem vai ajudar a eliminar o desperdício de dinheiro com hardware ocioso, ou seja, ao invés de termos que fazer o investimento em muitos servidores e deixar eles ligados mesmo quando o fluxo de pedidos for menor, temos um sistema que irá ajustar isso automaticamente dependendo da necessidade. O principal ganho do uso dessa ferramenta é o uso eficiente da memória do sistema, garantindo uma economia monetária com relação ao uso de computadores e para além disso também garantindo que o sistema nunca trave por falta de memória.

Etapa 2: Otimização de Armazenamento e distribuição

- Amazon S3 Standart(Simple Storage Service)
- Responsável pelo armazenamento de objetos, ou seja, os arquivos do sistema de forma segura, barata e com grandes capacidades sem a necessidade de gerenciar discos rígidos físicos. Os objetos armazenados podem ser de qualquer tipo e vão sempre carregar consigo as informações chave (nome), valor (conteúdo) e metadados (pares nome-valor com informações do objeto). Em especial o formato Standard é projetado para dados acessados com frequência, como é o caso para sites de distribuição de conteúdo e análise de dados.
- Todos os documentos digitais, como PDFs de faturas, fotos de produtos e manuais serão movidos para dentro do sistema. Ao utilizar do S3 standart, temos a estrutura ideal para dados acessados com frequência, como é o caso para os arquivos de pedidos e a distribuição de conteúdo para diversas outras empresas, sendo uma classe versátil e adequada para a maiorida das necessidades de armazenamento de dados que precisem de acesso rápido e confiável. Como redução de custo, o custo por GB no S3 é extremamente baixo se comparado a manter servidores de arquivos locais. O principal ganho que teremos é a alta disponibilidade dos dados, onde as farmacias parceiras vão conseguir baixar os catálogos via internet com velocidade, sem que a distribuidora (nós) precise investir em infraestrutura de rede complexa.

Etapa 3: Redução de Custo Operacional de Banco de Dados

- Amazon RDS
- Serviço de banco de dados SQL gerenciado que automatiza tarefas complexas como backups, atualizações de segurança e correções de erro.
- Migraremos o banco de dados de inventário (medicamentos, lotes e validades) para o RDS. Assim, o serviço cuidará sozinho das atualizações diárias dos dados para segurança. Tal aplicação irá reduzir os custos de mão de obra e de riscos, pois como a AWS automatiza a manutenção do sistema, a equipe de TI pode focar em vender mais em vez de gastar horas corrigindo o banco de dados. Isso também vai evitar multas ou perdas financeiras por bancos de dados fora do ar. Tal aplicação terá como benefício manter a continuidade do negócio, e caso houver falhas o RDS vai ser capaz de recuperar os dados rapidamente, garantindo que o hub de distribuição nunca parece operar por problemas técnicos no estoque.



## Conclusão
A implementação de ferramentas na empresa *Abstergo Industries tem como esperado uma economia de custos, além da automação de serviços essenciais para o funcionamento do negócio como um todo, melhorando a capacidade do sistema de receber grandes volumes de dado*, o que aumentará a eficiência e a produtividade da empresa. Recomenda-se a continuidade da utilização das ferramentas implementadas e a busca por novas tecnologias que possam melhorar ainda mais os processos da empresa.

## Anexos

Assinatura do Responsável pelo Projeto:

Pedro Gonçalves
