# kube-bench

![Version: 0.1.0](https://img.shields.io/badge/Version-0.1.0-informational?style=flat-square)

Helm chart to deploy run kube-bench as a cronjob on gke or eks.

**Homepage:** <https://github.com/aquasecurity/kube-bench>

## How to install this chart

Add Lemontech public chart repo:

```console
helm repo add lemontech TBD
```

A simple install with default values:

```console
helm install lemontech/kube-bench
```

To install the chart with the release name `my-release`:

```console
helm install my-release lemontech/kube-bench
```

To install with some set values:

```console
helm install my-release lemontech/kube-bench --set values_key1=value1 --set values_key2=value2
```

To install with custom values file:

```console
helm install my-release lemontech/kube-bench -f values.yaml
```

## Source Code

* <https://github.com/aquasecurity/kube-bench>

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| concurrencyPolicy | string | `"Forbid"` |  |
| cronjob.command | list | `[]` |  |
| cronjob.schedule | string | `"0 0 1 * *"` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"aquasec/kube-bench"` |  |
| image.tag | string | `"0.4.0"` |  |
| nodeSelector | object | `{}` |  |
| provider | string | `"eks"` |  |
| resources | object | `{}` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.create | bool | `false` |  |
| tolerations | list | `[]` |  |

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| raulsh | <rsalamanca@lemontech.com> |  |
