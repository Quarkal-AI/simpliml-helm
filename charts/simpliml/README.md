# SimpliML helm chart

[SimpliML documentation](https://simpliml.tech/documentation/)

## TLDR

```bash
helm repo add simpliml https://quarkal-ai.github.io/simpliml-helm
helm repo update
helm upgrade -i your-simpliml-installation-name simpliml/simpliml
```

## Description

This chart installs and bootstraps a SimpliML instance.

## Prerequisites

- Kubernetes v1.24+ (as you need grpc probe)
- Helm
- PV provisioner (by the infrastructure)

## Installation & Setup

You can install the chart from source via:

```bash
helm upgrade -i your-simpliml-installation-name charts/simpliml
```

Uninstall via:

```bash
helm uninstall your-simpliml-installation-name
```

### Overrides
You can override any value in the SimpliML configuration by setting the Helm values under the key `env`. 