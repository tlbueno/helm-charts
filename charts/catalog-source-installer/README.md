# catalog-source-installer

An helm chart to deploy a catalog source.

The chart will:
- create a namespace
- deploy a catalog source

By default, the chart deploy the redhat operators catalog but you may override the default values to install other catalogs.

### How to use

Check [README.md](../../README.md) for repo installation details.

To install the chart, ie:
```sh
helm install my-catalog-source-chart tlbueno/catalog-source-installer
```

You may override the default values below by creating a yaml file with one or more entries and use it in helm command, ie:
```sh
helm install my-catalog-source-chart -f ./my-values.yaml tlbueno/catalog-source-installer
```

Default values:
```yaml
# Default values for catalog-soruce-installer.
# This is a YAML-formatted file.
# Declare variables to be passed into your templates.

catalogSource:
  # catalog name
  name: redhat-operators-catalog
  # namespace where to install
  namespace: olm
  # source type
  sourceType: grpc
  # catalog index image
  image: registry.redhat.io/redhat/redhat-operator-index:v4.16
  # catalog display name
  displayName: Redhat Operators Catalog
  # publisher
  published: RedHat
  # update interval
  updateInterval: 15m

```

