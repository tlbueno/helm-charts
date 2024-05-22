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

You can use the helm command below to list the available chars versions and apps versions
```sh
helm search repo tlbueno/amq-broker-operator-crds --versions
```

In the list below you can see that chart version 0.2.0 is related to app version 7.12.0.OPR.1 which is the operator version this chart is related to
```sh
NAME                            	CHART VERSION	APP VERSION 	DESCRIPTION                                     
tlbueno/amq-broker-operator-crds	0.2.0        	7.12.0.OPR.1	A Helm chart to install AMQ Broker Operator CRDs
tlbueno/amq-broker-operator-crds	0.1.0        	7.11.6.OPR.2	A Helm chart to install AMQ Broker Operator CRDs
```

Default values:
- Currently the chart do not have any default value.

