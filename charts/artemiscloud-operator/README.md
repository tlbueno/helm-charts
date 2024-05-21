# artemiscloud-operator

An helm chart to deploy the ArtemisCloud Operator

The chart will:
- create a namespace
- deploy the artemiscloud operator

### How to use

Check [README.md](../../README.md) for repo installation details.

To install the chart, ie:
```sh
helm install my-artemiscloud-operator tlbueno/artemiscloud-operator
```

You may override the default values below by creating a yaml file with one or more entries and use it in helm command, ie:
```sh
helm install my-artemiscloud-operator -f ./my-values.yaml tlbueno/artemiscloud-operator
```

Default values:
```yaml
# Default values for olm-operator-installer.
# This is a YAML-formatted file.
# Declare variables to be passed into your templates.

namespace:
  # namespace where the operator will be installed
  name: artemiscloud-operator

operator:
  watch:
    # operator watch namespace mode
    # expected one of the values:
    #   single: operator will watch only its own namespace
    #   multi: operator will watch the ones specified in namespaces below
    #   all: operator will watch all namespaces
    mode: all
    # list of namespaces to watch in case of multi namespace mode
    namespaces:
      # - my-sample-namespace-1
      # - my-sample-namespace-2
```

