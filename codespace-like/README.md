# helm-chart-codespace-like

![Version: 0.1.5](https://img.shields.io/badge/Version-0.1.5-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 0.5.2](https://img.shields.io/badge/AppVersion-0.5.2-informational?style=flat-square)

A Helm chart for deploying a codespace-like dev server

## Maintainers

| Name      | Email                   | URL |
| --------- | ----------------------- | --- |
| webofmars | <contact@webofmars.com> |     |
| escemi    | <contact@escemi.com>    |     |

## Values

| Key                                        | Type   | Default                                                       | Description |
| ------------------------------------------ | ------ | ------------------------------------------------------------- | ----------- |
| affinity                                   | object | `{}`                                                          |             |
| autoscaling.enabled                        | bool   | `false`                                                       |             |
| autoscaling.maxReplicas                    | int    | `100`                                                         |             |
| autoscaling.minReplicas                    | int    | `1`                                                           |             |
| autoscaling.targetCPUUtilizationPercentage | int    | `80`                                                          |             |
| docker.enabled                             | bool   | `false`                                                       |             |
| docker.image.repository                    | string | `"docker"`                                                    |             |
| docker.image.tag                           | string | `"dind"`                                                      |             |
| docker.resources                           | object | `{}`                                                          |             |
| fullnameOverride                           | string | `""`                                                          |             |
| image.pullPolicy                           | string | `"IfNotPresent"`                                              |             |
| image.repository                           | string | `"ghcr.io/hoverkraft-tech/docker-base-images/codespace-like"` |             |
| image.tag                                  | string | `""`                                                          |             |
| imagePullSecrets                           | list   | `[]`                                                          |             |
| ingress.annotations                        | object | `{}`                                                          |             |
| ingress.className                          | string | `""`                                                          |             |
| ingress.enabled                            | bool   | `false`                                                       |             |
| ingress.hosts[0].host                      | string | `"chart-example.local"`                                       |             |
| ingress.hosts[0].paths[0].path             | string | `"/"`                                                         |             |
| ingress.hosts[0].paths[0].pathType         | string | `"ImplementationSpecific"`                                    |             |
| ingress.tls                                | list   | `[]`                                                          |             |
| livenessProbe.httpGet.path                 | string | `"/healthz"`                                                  |             |
| livenessProbe.httpGet.port                 | string | `"http"`                                                      |             |
| nameOverride                               | string | `""`                                                          |             |
| namespace                                  | string | `nil`                                                         |             |
| nodeSelector                               | object | `{}`                                                          |             |
| persistence.enbaled                        | bool   | `true`                                                        |             |
| persistence.size                           | string | `"100Mi"`                                                     |             |
| persistence.storageClass                   | string | `""`                                                          |             |
| podAnnotations                             | object | `{}`                                                          |             |
| podLabels                                  | object | `{}`                                                          |             |
| podSecurityContext                         | object | `{}`                                                          |             |
| readinessProbe.httpGet.path                | string | `"/healthz"`                                                  |             |
| readinessProbe.httpGet.port                | string | `"http"`                                                      |             |
| replicaCount                               | int    | `1`                                                           |             |
| resources                                  | object | `{}`                                                          |             |
| securityContext                            | object | `{}`                                                          |             |
| service.port                               | int    | `8080`                                                        |             |
| service.type                               | string | `"ClusterIP"`                                                 |             |
| serviceAccount.annotations                 | object | `{}`                                                          |             |
| serviceAccount.automount                   | bool   | `true`                                                        |             |
| serviceAccount.create                      | bool   | `true`                                                        |             |
| serviceAccount.name                        | string | `""`                                                          |             |
| startupProbe.httpGet.path                  | string | `"/healthz"`                                                  |             |
| startupProbe.httpGet.port                  | string | `"http"`                                                      |             |
| tolerations                                | list   | `[]`                                                          |             |
| volumeMounts                               | list   | `[]`                                                          |             |
| volumes                                    | list   | `[]`                                                          |             |

---

Autogenerated from chart metadata using [helm-docs v1.14.2](https://github.com/norwoodj/helm-docs/releases/v1.14.2)
