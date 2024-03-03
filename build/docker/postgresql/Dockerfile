# Image-Base
FROM postgres:latest
LABEL maintainer="Gabriel Padilha <gabriel.padzx@outlook.com>"

# -- Metadatas 
ARG build_date
LABEL org.label-schema.build-date=${build_date}
LABEL org.label-schema.name="Apache Spark Standalone Cluster"
LABEL org.label-schema.description="PostgreSQL Image"
LABEL org.label-schema.url="https://github.com/Padzx/spark-standalone-postgresql-on-docker"
LABEL org.label-schema.schema-version="1.0"


# Expose the PostgreSQL Port
EXPOSE 5432

# Time Zone Location Settings
ENV TZ=UTC
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

COPY build/postgresql.conf /etc/postgresql/postgresql.conf

# RUN
CMD ["postgres"]
