FROM alpine:latest

ARG USER_UID=10001
USER ${USER_UID}

COPY gitlab /gitlab
COPY otelcol.yaml /etc/gitlab/config.yaml
ENTRYPOINT ["/gitlab"]
CMD ["--config", "/etc/gitlab/config.yaml"]
EXPOSE 4317
