# toolbox

An helm chart to create a toolbox pod

The chart will:
- create a namespace
- deploy a pod with the specified image

### How to use

Check [README.md](../../README.md) for repo installation details

To install the chart, ie:
```sh
helm install my-toolbox-chart tlbueno/toolbox
```

You may override the default values below by creating a yaml file with one or more entries and use it in helm command, ie:
```sh
helm install my-toolbox-chart -f ./my-values.yaml tlbueno/toolbox
```

Default values:
```yaml
# Default values for toolbox.
# This is a YAML-formatted file.
# Declare variables to be passed into your templates.

namespace:
  # namespace name
  name: toolbox

container:
  # image to be used in the pod
  image: quay.io/tlbueno/toolbox:latest
```

