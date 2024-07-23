# SimpliML helm repository
[SimpliML documentation](https://docs.simpliml.com)

This repository hosts the following helm charts:

* [SimpliML](charts/simpliml/README.md)

## Usage

```bash
helm repo add simpliml https://quarkal-ai.github.io/simpliml-helm
helm repo update
helm upgrade -i your-simpliml-installation-name simpliml/simpliml
```

For more in-depth usage documentation, see [the helm chart's README](charts/simpliml/README.md).

## Upgrading

This helm chart installs the latest version of SimpliML by default. When a new version of SimpliML is available, upgrade the helm chart with the following commands:

```bash
helm repo update
helm upgrade your-simpliml-installation-name simpliml/simpliml
```

This command performs a rolling upgrade of your SimpliML cluster, updating one node at a time.

If you have overridden the SimpliML image tag in `values.yaml`, you will also need to update that tag before running `helm upgrade`.

```yaml
image:
  tag: vX.Y.Z
```

## Contributing

See [CONTRIBUTING.md](./CONTRIBUTING.md).