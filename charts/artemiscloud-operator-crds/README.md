# artemiscloud-operator-crds

An helm chart to deploy the ArtemisCloud Operator CRDs

The chart will:
- deploy the CRDs

### How to use

Check [README.md](../../README.md) for repo installation details.

To install the chart, ie:
```sh
helm install my-artemiscloud-operator-crds tlbueno/artemiscloud-operator-crds
```

You may override the default values below by creating a yaml file with one or more entries and use it in helm command, ie:
```sh
helm install my-artemiscloud-operator-crds -f ./my-values.yaml tlbueno/artemiscloud-operator-crds
```

Default values:
- Currently the chart do not have any default value.

