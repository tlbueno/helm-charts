# arkmq-operator-crds

An helm chart to deploy the ArkMQ Operator CRDs

The chart will:
- deploy the CRDs

### How to use

Check [README.md](../../README.md) for repo installation details.

To install the chart, ie:
```sh
helm install my-arkmq-operator-crds tlbueno/arkmq-operator-crds
```

You may override the default values below by creating a yaml file with one or more entries and use it in helm command, ie:
```sh
helm install my-arkmq-operator-crds -f ./my-values.yaml tlbueno/arkmq-operator-crds
```

You can use the helm command below to list the available chars versions and apps versions
```sh
helm search repo tlbueno/arkmq-operator-crds --versions
```

Default values:
- Currently the chart do not have any default value.

