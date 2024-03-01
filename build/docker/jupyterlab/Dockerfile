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

# Install JAVA 
RUN apt-get update && apt-get install -y default-jre

# COPY requirements.txt and install dependencies
COPY build/requirements.txt /app/requirements.txt
RUN pip3 install --no-cache-dir -r /app/requirements.txt

# Install Python and required packages
RUN apt-get install -y python3 python3-pip && \
    pip3 install jupyterlab findspark

# Set environment variables
ENV SPARK_HOME /usr/local/lib/python3.9/site-packages/pyspark
ENV PATH $SPARK_HOME/bin:$PATH

# Install PySpark
RUN pip3 install pyspark

# Configure PySpark environment
ENV PYSPARK_PYTHON python3
ENV PYSPARK_DRIVER_PYTHON jupyter
ENV PYSPARK_DRIVER_PYTHON_OPTS "lab --ip=0.0.0.0 --port=8888 --allow-root"

# Create Python kernel for PySpark
RUN python3 -m ipykernel install --user --name=python3 --display-name="PySpark"

# Expose JupyterLab port
EXPOSE 8888

# Defaul dir
WORKDIR /app

# Start JupyterLab
CMD ["jupyter", "lab"]