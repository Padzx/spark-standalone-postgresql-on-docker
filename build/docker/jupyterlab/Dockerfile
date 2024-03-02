# Image-Base
FROM padzx/jdk_base
LABEL maintainer="Gabriel Padilha <gabriel.padzx@outlook.com>"

# -- Metadatas 
ARG build_date
LABEL org.label-schema.build-date=${build_date}
LABEL org.label-schema.name="Apache Spark Standalone Cluster"
LABEL org.label-schema.description="Jupyterlab Image"
LABEL org.label-schema.url="https://github.com/Padzx/spark-standalone-postgresql-on-docker"
LABEL org.label-schema.schema-version="1.0"

# Install JAVA 
RUN apt-get update && apt-get install -y default-jre

# Install Python and required packages
RUN apt-get install -y python3 python3-pip && \
    pip3 install --no-cache-dir jupyterlab findspark dash plotly pandas matplotlib psycopg2-binary pyspark numpy scikit-learn tensorflow

# Set environment variables for Spark
ENV SPARK_HOME /usr/local/spark
ENV PATH $SPARK_HOME/bin:$PATH

# Configure PySpark environment
ENV PYSPARK_PYTHON python3
ENV PYSPARK_DRIVER_PYTHON jupyter
ENV PYSPARK_DRIVER_PYTHON_OPTS "lab --ip=0.0.0.0 --port=8888 --allow-root"

# Copy Spark binaries from Spark image
COPY --from=padzx/spark-master:latest /usr/bin/spark /usr/local/spark

# Create Python kernel for PySpark
RUN python3 -m ipykernel install --user --name=python3 --display-name="PySpark"

# Expose JupyterLab port
EXPOSE 8888

# Default directory
WORKDIR /app

# Start JupyterLab with --allow-root
CMD ["jupyter", "lab", "--ip=0.0.0.0", "--port=8888", "--allow-root"]
