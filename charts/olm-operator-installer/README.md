# olm-operator-installer

An helm chart to install an operator using Operator Lifecycle Manager (OLM)

The chart will:
- create a namespace
- deploy an operator group with/without a selector label defined in the values
- deploy the subscription

By default, the chart deploy a cert-manager operator. But you can find some more examples in [examples](./examples) folder

### How to use

Check [README.md](../../README.md) for repo installation details

To install the chart, ie:
```sh
helm install my-operator-chart tlbueno/olm-operator-installer
```

You may override the default values below by creating a yaml file with one or more entries and use it in helm command, ie:
```sh
helm install my-operator-chart -f ./my-values.yaml tlbueno/olm-operator-installer
```

Default values:
```yaml
# Default values for olm-operator-installer.
# This is a YAML-formatted file.
# Declare variables to be passed into your templates.

namespace:
  # namespace where the operator will be installed
  name: cert-manager

operatorGroup:
  # skip the operator group deploy if false
  deploy: true
  # operator group name
  name: cert-manager-operator

  selector:
    # do not set selector matchLabels if false
    enabled: false
    # A list of maps with the labels
    matchLabels:
      - name: olm-operator-installer/managed-by
        value: "{{ .Values.subscription.name }}"

subscription:
  # subscription name
  name: cert-manager-operator-sub

  # channel name
  channel: stable

  # operator package name
  operatorName: cert-manager

  # catalog name from which the operator will be installed
  source: operatorhubio-catalog

  # catalog namespace
  sourceNamespace: olm

  # install plan approval type
  installPlanApproval: Automatic
  
  # the initial version of the operator to be installed
  # if empty it will not be used in the subscription 
  startingCSV: ""
```

