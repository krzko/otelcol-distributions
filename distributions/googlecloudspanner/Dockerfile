FROM alpine:latest

ARG USER_UID=10001
USER ${USER_UID}

COPY googlecloudspanner /googlecloudspanner
COPY otelcol.yaml /etc/googlecloudspanner/config.yaml
ENTRYPOINT ["/googlecloudspanner"]
CMD ["--config", "/etc/googlecloudspanner/config.yaml"]
EXPOSE 4317
