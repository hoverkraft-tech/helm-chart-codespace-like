# <img src=".github/logo.svg" width="56" alt="" /> Codespace Like Helm Chart

Run a personal, browser-based development workspace on your Kubernetes cluster.

[![Continuous Integration](https://github.com/hoverkraft-tech/helm-chart-codespace-like/actions/workflows/main-ci.yml/badge.svg)](https://github.com/hoverkraft-tech/helm-chart-codespace-like/actions/workflows/main-ci.yml)
[![Release](https://img.shields.io/github/v/release/hoverkraft-tech/helm-chart-codespace-like)](https://github.com/hoverkraft-tech/helm-chart-codespace-like/releases)
[![PRs welcome](https://img.shields.io/badge/PRs-welcome-brightgreen)](docs/development/linting.md)

## Prerequisites

A Kubernetes cluster, a configured kubectl context and Helm with OCI registry support. Persistent storage and an ingress controller are needed when enabling those features.

## Install

Review the [chart values](codespace-like/values.yaml), save your settings in `my-values.yaml`,
then install a published chart:

```sh
helm upgrade --install codespace-like oci://ghcr.io/hoverkraft-tech/helm-chart-codespace-like/charts/codespace-like/helm-chart-codespace-like \
  --namespace codespace-like --create-namespace \
  --values my-values.yaml
```

See [usage and configuration](docs/usage/installation.md) for more details.

## Contributing

Open an issue or pull request to discuss changes. The [contributor guide](docs/development/linting.md)
describes the dev container and local lint commands.

## Maintainer

Maintained by [Hoverkraft](https://hoverkraft.cloud).

## License

This repository does not currently provide a top-level license.
Bundled third-party code retains its own license.
