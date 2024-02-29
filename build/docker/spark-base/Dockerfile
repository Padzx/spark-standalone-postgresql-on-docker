# Image-Base: OpenJdk11
FROM padzx/jdk_base:latest 
LABEL maintainer="Gabriel Padilha <gabriel.padzx@outlook.com>"

# -- Metadatas
ARG build_date
LABEL org.label-schema.build-date=${build_date}
LABEL org.label-schema.name="Apache Spark Standalone Cluster"
LABEL org.label-schema.description="Spark-Base Image"
LABEL org.label-schema.url="https://github.com/Padzx/spark-standalone-postgresql-on-docker"
LABEL org.label-schema.schema-version="1.0"

# Download and install Apache Spark
RUN curl -L https://archive.apache.org/dist/spark/spark-3.5.0/spark-3.5.0-bin-hadoop3.tgz -o spark.tgz && \
    tar -xf spark.tgz && \
    mv spark-3.5.0-bin-hadoop3 /usr/bin/spark && \
    echo "alias pyspark=/usr/bin/spark/bin/pyspark" >> ~/.bashrc && \
    echo "alias spark-shell=/usr/bin/spark/bin/spark-shell" >> ~/.bashrc && \
    mkdir /usr/bin/spark/logs && \
    rm spark.tgz

# Copy PostgreSQL JDBC Driver to Spark JARs directory
COPY build/drivers/postgresql-42.7.2.jar /usr/bin/spark/jars/

# Set environment variables
ENV SPARK_HOME /usr/bin/spark
ENV SPARK_MASTER_HOST spark-master
ENV SPARK_MASTER_PORT 7077
ENV PYSPARK_PYTHON python3

# Set working directory
WORKDIR ${SPARK_HOME}
