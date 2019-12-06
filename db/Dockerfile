FROM postgres:12.0-alpine

ARG DB_DIALECT
ARG DB_RESTORE
ARG POSTGRES_DB
ARG POSTGRES_USER

ENV DB_DIALECT=${DB_DIALECT}
ENV DB_RESTORE=${DB_RESTORE}
ENV POSTGRES_DB=${POSTGRES_DB}
ENV POSTGRES_USER=${POSTGRES_USER}

# Add a script to a special location inside the container, which will be
# executed when the container is up and running.
ADD ./db_restore.sh /docker-entrypoint-initdb.d
EXPOSE 5432