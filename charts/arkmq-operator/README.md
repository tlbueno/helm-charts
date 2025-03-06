# arkmq-operator

An helm chart to deploy the ArkMQ Operator

The chart will:
- create a namespace
- deploy arkmq operator CRDs (optional)
- deploy the arkmq operator

### How to use

Check [README.md](../../README.md) for repo installation details.

To install the chart, ie:
```sh
helm install my-arkmq-operator tlbueno/arkmq-operator
```

You may override the default values below by creating a yaml file with one or more entries and use it in helm command, ie:
```sh
helm install my-arkmq-operator -f ./my-values.yaml tlbueno/arkmq-operator
```

You can use the helm command below to list the available chars versions and apps versions
```sh
helm search repo tlbueno/arkmq-operator --versions
```

Default values:
```yaml
# Default values for arkmq-operator.
# This is a YAML-formatted file.
# Declare variables to be passed into your templates.

# If true it will deploy the dependency chart arkmq-operator-crds
# If false it will skip the dependency install. In this case the CRD must be already installed
# Setting this as false and installing the arkmq-operator-crds before
# will let you manage the CRD versions in a different helm release, so, in this case
# you can have different versions of the operator at the same time.
# as an example, you can install arkmq-operator-crds for operator 1.2.1,
# then install the arkmq-operator for operator 1.2.1,
# then install the arkmq-operator for operator 1.1.0 in a different namespace
# as the CRDs have backward compatibility and you installed the latest one,
# you can have multiple operator versions at the same time but you need to ensure they are
# watching specific namespaces otherwise it can have unexpected behavior
installCrds: true

operator:
  # Operator log level
  logLevel: info

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

