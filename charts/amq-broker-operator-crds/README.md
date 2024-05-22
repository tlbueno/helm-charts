# amq-broker-operator-crds

An helm chart to deploy the AMQ Broker Operator CRDs

The chart will:
- deploy the CRDs

### How to use

Check [README.md](../../README.md) for repo installation details.

To install the chart, ie:
```sh
helm install my-amq-broker-operator-crds tlbueno/amq-broker-operator-crds
```

You may override the default values below by creating a yaml file with one or more entries and use it in helm command, ie:
```sh
helm install my-amq-broker-operator-crds -f ./my-values.yaml tlbueno/amq-broker-operator-crds
```

Default values:
- Currently the chart do not have any default value.

