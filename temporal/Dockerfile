FROM temporalio/auto-setup:1.20.3

ENV DB postgresql
ENV DB_PORT 5432
ENV POSTGRES_USER temporal
ENV POSTGRES_PWD temporal
ENV POSTGRES_SEEDS postgresql
ENV DYNAMIC_CONFIG_FILE_PATH config/dynamicconfig/development-sql.yaml
ENV ENABLE_ES true
ENV ES_SEEDS elasticsearch
ENV ES_VERSION v7
ENV PROMETHEUS_ENDPOINT 0.0.0.0:8000

COPY ./config_template.yaml /etc/temporal/config/config_template.yaml

RUN echo "NOW WITH OPEN TELEMETRY"