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

You can use the helm command below to list the available chars versions and apps versions
```sh
helm search repo tlbueno/artemiscloud-operator-crds --versions
```

In the list below you can see that chart version 0.2.1 is related to app version 1.2.1 which is the operator version this chart is related to
```sh
NAME                              	CHART VERSION	APP VERSION	DESCRIPTION                                       
tlbueno/artemiscloud-operator-crds	0.2.1        	1.2.1      	A Helm chart to install ArtemisCloud Operator CRDs
tlbueno/artemiscloud-operator-crds	0.2.0        	1.2.0      	A Helm chart to install ArtemisCloud Operator CRDs
tlbueno/artemiscloud-operator-crds	0.1.0        	1.1.0      	A Helm chart to install ArtemisCloud Operator CRDs
```
* From version 1.2.5 chart version and app version will match. This means, chart version 1.2.5 will install operator version 1.2.5

Default values:
- Currently the chart do not have any default value.

