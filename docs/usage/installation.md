# Installation and configuration

## Published charts

The chart is published at `oci://ghcr.io/hoverkraft-tech/helm-chart-codespace-like/charts/codespace-like/helm-chart-codespace-like`.
Choose a version from the [releases](https://github.com/hoverkraft-tech/helm-chart-codespace-like/releases)
and add `--version <chart-version>` when you need a reproducible deployment.

The [chart reference](../../codespace-like/README.md) and
[values file](../../codespace-like/values.yaml) describe the supported configuration.
Keep secrets outside Git and protect any local values file containing credentials.

## Install from source

From the repository root:

```sh
helm dependency build codespace-like
helm upgrade --install codespace-like ./codespace-like \
  --namespace codespace-like --create-namespace \
  --values my-values.yaml
```
