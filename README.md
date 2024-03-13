# otelcol-distributions

This repository is dedicated to custom distributions of the OpenTelemetry Collector, tailored to meet specific observability needs. The current ones you can find are:

* **GitHub Actions:** Tailored to capture and analyse events from GitHub workflows and jobs, facilitating better insights into CI/CD processes.
* **GitLab:** Focused on GitLab-specific events, enabling comprehensive observability across GitLab CI/CD pipelines and builds.
* **Google Cloud Spanner:** Customised to observe Google Spanner database metrics, with the addition of [fine-grained access control for Spanner databases](https://cloud.google.com/spanner/docs/configure-fgac).

## Getting Started

### Docker

...

## Adding a new distribution

To add a new distribution to this repository:

1. create a directory under `distributions` and place the `manifest.yaml` there
2. add `./github/workflows/ci-<distribution>.yaml` and `./github/workflows/release-<distribution>.yaml` files based on one of the existing distributions

You can test your new distribution with:

```sh
./test/test.sh -d YOUR_DISTRIBUTION
```

Or, to run everything the CI would run:

```sh
make ci
```
