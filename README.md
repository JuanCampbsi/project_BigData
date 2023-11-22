
### Desenvolvimento e Avaliação de uma Arquitetura Distribuída para o Cadastro Ambiental Rural no Databricks

Alunos: Juan, Bernardo, Rafael, Jhonata

Este projeto tem como objetivo explorar as capacidades de arquiteturas de bancos de dados distribuídos, utilizando tecnologias avançadas como Apache Spark e Databricks, com foco no Cadastro Ambiental Rural. A proposta envolve a criação, implementação e avaliação de uma arquitetura distribuída que integra o poder de processamento do Spark e a flexibilidade do Databricks. Essa abordagem permitirá uma migração eficiente dos dados armazenados no Databricks File System (DBFS), além de facilitar a realização de testes comparativos. O objetivo é otimizar o gerenciamento e análise dessas informações, aproveitando a escalabilidade e o desempenho dessas tecnologias para lidar com grandes volumes de dados de maneira eficiente e eficaz.


### Fonte de dados 

Instalação no ambiente databrics

```bash
%sh
  curl https://dados.agricultura.gov.br/dataset/58bdc09c-9778-42b9-8fce-7d5c2c4fa211/resource/daf8053b-5446-4cd4-986a-f141b4a434ec/download/temas_ambientais.csv --output /tmp/temas_ambientais.csv
```

Movendo csv para o dbfs
```bash
dbutils.fs.mv("file:/tmp/temas_ambientais.csv", "dbfs:/FileStore/Projeto/temas_ambientais.csv")
```