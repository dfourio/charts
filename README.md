# dføur Charts
[![Release Charts on demand](https://github.com/dfourio/charts/actions/workflows/release-ondemand.yaml/badge.svg)](https://github.com/dfourio/charts/actions/workflows/release-ondemand.yaml)

This repository contains the charts used for installing [dføur](https://dfour.space) using Helm. Currently, this chart only contains the following chart:

- `dfour-hub` - The chart for a dføur-hub. For the actual dføur repository, [go here](https://github.com/cividi/spatial-data-package-platform).

## Adding the Chart
```
$ helm repo add dfour https://dfourio.github.io/charts/
$ helm repo update
```

## Releasing New Charts
When ready to release a new chart version or add a new chart, copy the chart directory from the source repository into the `charts/` directory. Make sure the chart directory is named after the actual chart (for example: `dfour-hub/`).

Once pushed, GitHub Actions will look for any changes to charts in the `charts/` directory since the last tagged release in the repository, package any changed charts, and then release them on `GitHub Pages`.

Note that changes should only be synced to this repository when ready for a new release. GitHub Actions will fail if making changes to the charts in this repository directly, as Chart Releaser will not attempt to override old chart releases.
