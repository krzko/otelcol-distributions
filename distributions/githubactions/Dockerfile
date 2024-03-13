FROM alpine:latest

ARG USER_UID=10001
USER ${USER_UID}

COPY githubactions /githubactions
COPY otelcol.yaml /etc/githubactions/config.yaml
ENTRYPOINT ["/githubactions"]
CMD ["--config", "/etc/githubactions/config.yaml"]
EXPOSE 4317
