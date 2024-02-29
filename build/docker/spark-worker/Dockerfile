FROM padzx/spark_base:latest
LABEL manteiner="Gabriel Padilha <gabriel.padzx@outlook.com>"

# -- Metadatas --

ARG build_date

LABEL org.label-schema.build-date=${build_date}
LABEL org.label-schema.name="Apache Spark Standalone Cluster"
LABEL org.label-schema.description="Spark-Base Image"
LABEL org.label-schema.url="https://github.com/Padzx/spark-standalone-postgresql-on-docker"
LABEL org.label-schema.schema-version="1.0"

# -- Runtime

EXPOSE 8081

CMD bin/spark-class org.apache.spark.deploy.worker.Worker spark://${SPARK_MASTER_HOST}:${SPARK_MASTER_PORT} >> logs/spark-worker.out
