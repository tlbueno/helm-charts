# broker-operator

An helm chart to install the AMQ Broker Operator using Operator Lifecycle Manager (OLM)

The chart will:
- create a namespace with label named broker-operator/managed-by filled with the subscription name
- deploy an operator group with a selector label named broker-operator/managed-by filled with the subscription name
- deploy the subscription

### How to use

Check [README.md](../../README.md) for repo installation details

To install the chart use the command:
```sh
helm install broker-operator tlbueno-repo/broker-operator
```

You may override the default values below by creating a yaml file with one or more entries and use it in helm command, ie:
```sh
helm install broker-operator -f ./my-values.yaml tlbueno-repo/broker-operator
```

Default values:
```yaml
# Default values for broker-operator.
# This is a YAML-formatted file.
# Declare variables to be passed into your templates.

# namespace where the operator will be installed
namespace: broker-operator-olm

operatorGroup:
  # operator group name
  name: broker-operator

subscription:
  # subscription name
  name: broker-operator-olm-sub

  # channel name
  channel: 7.11.x

  # operator package name
  operatorName: amq-broker-rhel8

  # catalog name from which the operator will be installed
  source: redhat-operators-catalog

  # catalog namespace
  sourceNamespace: olm

  # install plan approval type
  installPlanApproval: Automatic
  
  # the initial version of the operator to be installed
  # if empty it will not be used in the subscription 
  startingCSV: ""
```

