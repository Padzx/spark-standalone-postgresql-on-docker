# Apache Spark Standalone Cluster PostgreSQL on Docker

## Summary 

- [Introduction](#introduction)
- [Seção 2](#seção-2)
- [Seção 3](#seção-3)

## Introduction

This project was built with the aim of showing how a distributed environment can be highly powerful in situations involving data analysis with the appropriate tools for use, the project has the intention of showing that dealing with large volumes of data in highly scalable and Resilient systems can become a much more efficient and productive task in real workload situations. Using tools such as **Jupyter Notebook**, **Spark Clusters** and **PostgreSQL** further helps the knowledge of how each real task with data works in a production line.


## ETL (Extract, Transform and Load)

In this Project we use Clusters (Master, Worker) as ETL processes, an extremely powerful and versatile tool (can be worked on involving scalability with tools such as Kubernetes and cloud applications), with Spark we can create extremely efficient and performant ETL workloads.

> **Note:** To learn more about ETL [Click Here](https://www.oracle.com/ph/integration/what-is-etl/).


## Starting Docker Containers

To initialize docker containers, you must be in the project's root directory and then execute:

```bash
docker-compose up
```

detached mode:

```bash
docker-compose up -d
```









