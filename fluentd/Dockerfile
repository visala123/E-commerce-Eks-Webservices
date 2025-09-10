# FROM fluentd
# USER root
# RUN apk update && \
#     apk add --virtual .build-dependencies build-base ruby-dev

# RUN fluent-gem install fluent-plugin-elasticsearch && \
#     fluent-gem install fluent-plugin-kubernetes_metadata_filter  && \
#     fluent-gem install fluent-plugin-multi-format-parser

FROM fluent/fluentd:v1.16-debian
USER root
RUN apt-get update && \
    apt-get install -y build-essential ruby-dev && \
    rm -rf /var/lib/apt/lists/*

RUN fluent-gem install fluent-plugin-elasticsearch && \
    fluent-gem install fluent-plugin-kubernetes_metadata_filter && \
    fluent-gem install fluent-plugin-multi-format-parser

