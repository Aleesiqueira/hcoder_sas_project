# Resolução Teste técnico – Pessoa Engenheira de Dados

## Especificações do desenvolvimento

* Linguagems: PySpark e SQL
* Ferramentas: Google Colab e BigQuery

## Instruções para execução do programa

* Abrir o código em um executor de Python Notebooks (https://colab.research.google.com/)
* Importar o arquivo data_question.json
* Clicar para executar todo o programa
* Ao executar a célula de conexão com o BigQuery, será necessário clicar no link que aparecerá no resultado, fazer login e copiar o token de autenticação para inserir na execução do código
  * Login: dataenginner.hcoder.test@gmail.com
  * Senha: SAS_2020

## Considerações sobre o armazenamento

  Ao importar o json e separar os dados de forma que pudessem ser armazenados sem perder a capacidade de se relacionarem e serem consultados, tive a ideia de utilizar o BigQuery como base de dados, por ser um ambiente totalmente escalável, distribuído, com auto poder de controle administrativo e dimensionamento computacional.
  
  Então, além de criar o schema do json que o programa importa, criei também as tabelas presentes no recorte do banco de dados de avaliações, para que pudesse consumi-las durante o código e utilizá-las no Desafio 2; inseri também alguns registros de teste nessas tabelas para que o join trouxesse algo relevante.

## Considerações sobre o dado

* Desafio 2
  * Na tabela de propriedades, o campo id é único, portanto no agrupamento do Desafio 2 nenhuma propriedade aparece com o campo property_size > 1. Para que as propriedades com nomes iguais sejam agrupadas, teria que utilizar o campo key.
