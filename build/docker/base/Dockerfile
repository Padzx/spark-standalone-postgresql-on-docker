# OpenJDK 11 as the Base Image
ARG debian_buster_image_tag=11-jre-slim
FROM openjdk:${debian_buster_image_tag}
LABEL manteiner: "Gabriel Padilha <gabriel.padzx@outlook.com>" 

# -- Metadatas --
ARG build_date

LABEL org.label-schema.build-date=${build_date}
LABEL org.label-schema.name="Apache Spark Standalone Cluster"
LABEL org.label-schema.description="Base JDK For Spark"
LABEL org.label-schema.url="https://github.com/Padzx/spark-standalone-postgresql-on-docker"
LABEL org.label-schema.schema-version="1.0"

# -- Layer: OS 

ARG shared_workspace=/opt/workspace

RUN mkdir -p ${shared_workspace}/data && \
    mkdir -p /usr/share/man/man1 && \
    apt-get update -y && \
    apt-get install -y curl python3 && \
    ln -s /usr/bin/python3 /usr/bin/python && \
    rm -rf /var/lib/apt/lists/*

ENV SHARED_WORKSPACE=${shared_workspace}

# -- RUN

VOLUME ${shared_workspace}
CMD ["bash"]
