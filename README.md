
### Development and Evaluation of a Distributed Architecture for Rural Environmental Registration in Databricks


This project aims to explore the capabilities of distributed database architectures, using advanced technologies such as Apache Spark and Databricks, with a focus on the Rural Environmental Registry. The proposal involves the creation, implementation and evaluation of a distributed architecture that integrates the processing power of Spark and the flexibility of Databricks. This approach will allow an efficient migration of data stored in the Databricks File System (DBFS), in addition to facilitating the performance of comparative tests. The goal is to optimize the management and analysis of this information, taking advantage of the scalability and performance of these technologies to deal with large volumes of data efficiently and effectively.


### Data source

Installation in Databricks environment

```bash
%sh
  curl https://dados.agricultura.gov.br/dataset/58bdc09c-9778-42b9-8fce-7d5c2c4fa211/resource/daf8053b-5446-4cd4-986a-f141b4a434ec/download/temas_ambientais.csv --output /tmp/temas_ambientais.csv
```

Moving csv to dbfs
```bash
dbutils.fs.mv("file:/tmp/temas_ambientais.csv", "dbfs:/FileStore/Projeto/temas_ambientais.csv")
```
