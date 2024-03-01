FROM padzx/spark_base:latest
LABEL maintainer="Gabriel Padilha <gabriel.padzx@outlook.com>"

# -- Metadatas

ARG build_date

LABEL org.label-schema.build-date=${build_date}
LABEL org.label-schema.name="Apache Spark Standalone Cluster"
LABEL org.label-schema.description="Spark-Base Image"
LABEL org.label-schema.url="https://github.com/Padzx/spark-standalone-postgresql-on-docker"
LABEL org.label-schema.schema-version="1.0"

# -- Runtime

EXPOSE 8080 7077

CMD bin/spark-class org.apache.spark.deploy.master.Master >> logs/spark-master.out