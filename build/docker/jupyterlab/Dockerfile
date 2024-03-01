# Image-Base
FROM padzx/jdk_base
LABEL maintainer = "Gabriel Padilha <gabriel.padzx@outlook.com>"

# -- Metadatas 

ARG build_date
LABEL org.label-schema.build-date=${build_date}
LABEL org.label-schema.name="Apache Spark Standalone Cluster"
LABEL org.label-schema.description="Jupyterlab Image"
LABEL org.label-schema.url="https://github.com/Padzx/spark-standalone-postgresql-on-docker"
LABEL org.label-schema.schema-version="1.0"

# Instal JAVA

RUN apt-get update && apt-get install -y defaullt-jre

# Instal Python and required packages
RUN apt-get install -y pytohn3 python3-pip && 