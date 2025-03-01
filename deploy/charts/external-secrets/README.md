# External Secrets

<p align="left"><img src="https://raw.githubusercontent.com/external-secrets/external-secrets/main/assets/round_eso_logo.png" width="100x" /></p>

[//]: # (README.md generated by gotmpl. DO NOT EDIT.)

![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![Version: 0.4.1](https://img.shields.io/badge/Version-0.4.1-informational?style=flat-square)

External secret management for Kubernetes

## TL;DR
```bash
helm repo add external-secrets https://charts.external-secrets.io
helm install external-secrets/external-secrets
```

## Installing the Chart
To install the chart with the release name `external-secrets`:
```bash
helm install external-secrets external-secrets/external-secrets
```

### Custom Resources
By default, the chart will install external-secrets CRDs, this can be controlled with `installCRDs` value.

## Uninstalling the Chart
To uninstall the `external-secrets` deployment:
```bash
helm uninstall external-secrets
```
The command removes all the Kubernetes components associated with the chart and deletes the release.

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| concurrent | int | `1` | Specifies the number of concurrent ExternalSecret Reconciles external-secret executes at a time. |
| controllerClass | string | `""` | If set external secrets will filter matching Secret Stores with the appropriate controller values. |
| deploymentAnnotations | object | `{}` | Annotations to add to Deployment |
| extraArgs | object | `{}` |  |
| extraEnv | list | `[]` |  |
| fullnameOverride | string | `""` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"ghcr.io/external-secrets/external-secrets"` |  |
| image.tag | string | `""` | The image tag to use. The default is the chart appVersion. |
| imagePullSecrets | list | `[]` |  |
| installCRDs | bool | `true` | If set, install and upgrade CRDs through helm chart. |
| leaderElect | bool | `false` | If true, external-secrets will perform leader election between instances to ensure no more than one instance of external-secrets operates at a time. |
| nameOverride | string | `""` |  |
| nodeSelector | object | `{}` |  |
| podAnnotations | object | `{}` | Annotations to add to Pod |
| podLabels | object | `{}` |  |
| podSecurityContext | object | `{}` |  |
| priorityClassName | string | `""` | Pod priority class name. |
| prometheus.enabled | bool | `false` | Specifies whether to expose Service resource for collecting Prometheus metrics |
| prometheus.service.port | int | `8080` |  |
| rbac.create | bool | `true` | Specifies whether role and rolebinding resources should be created. |
| replicaCount | int | `1` |  |
| resources | object | `{}` |  |
| scopedNamespace | string | `""` | If set external secrets are only reconciled in the provided namespace |
| securityContext | object | `{}` |  |
| serviceAccount.annotations | object | `{}` | Annotations to add to the service account. |
| serviceAccount.create | bool | `true` | Specifies whether a service account should be created. |
| serviceAccount.name | string | `""` | The name of the service account to use. If not set and create is true, a name is generated using the fullname template. |
| tolerations | list | `[]` |  |
