# dføur Chart

> **Warning**: dføur doesn't fully support downgrading from a higher version to a lower version.

## Source Code

dføur is 100% open source software. Project source code is currently maintaiuned as a mono-repo as:

1. Spatial Data Package Platform -- https://github.com/cividi/spatial-data-package-platform

## Prerequisites

1. A container runtime compatible with Kubernetes (Docker v1.13+, containerd v1.3.7+, etc.)
2. Kubernetes v1.18+

## Installation
1. Add dføur chart repository.
```
helm repo add dfour https://charts.dfour.io
```

2. Update local dfour chart information from chart repository.
```
helm repo update
```

3. Install dføur chart.
- With Helm 2, the following command will create a `dføur` namespace and install the dføur chart together.
```
helm install dfour-hub/dfour-hub --name dfour-hub --namespace dfour
``` 
- With Helm 3, the following commands will create the `dfour` namespace first, then install the dføur chart.

```
kubectl create namespace dfour
helm install dfour-hub dfour-hub/dfour-hub --namespace dfour
```

## Uninstallation

With Helm 2 to uninstall dføur.
```
helm delete dfour-hub --purge
```

With Helm 3 to uninstall dføur.
```
helm uninstall dfour-hub -n dfour
kubectl delete namespace dfour
```

---
Please see [link](https://github.com/cividi/spatial-data-package-platform) for more information.