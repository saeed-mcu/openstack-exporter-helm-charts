# Helm Chart for OpenStack Exporter

## Description

This is the official Helm Chart for [OpenStack Exporter](https://github.com/openstack-exporter/openstack-exporter), a tool to export Prometheus metrics from a running OpenStack Cloud.

## Configuration

The chart configuration is done in the `values.yaml` file.

## Usage

```bash
# Get a local copy
git clone https://github.com/openstack-exporter/helm-charts.git

# Package the chart
cd helm-charts/charts/prometheus-openstack-exporter/
helm package .

# Get chart version & install
version="$(awk '/^version:/{ print $NF }' Chart.yaml)"
helm install prometheus-openstack-exporter prometheus-openstack-exporter-${version}.tgz
```

## Contributing

Please fill pull requests or issues under Github.



## OpenStack volumes can be in the following states:
openstack_cinder_volume_status:

|   Status            |  Value  |
|---------------------|---------|
|"creating"           |   0     |
|"available"          |   1     |
|"reserved"           |   2     |
|"attaching"          |   3     |
|"detaching"          |   4     |
|"in-use"             |   5     |
|"maintenance"        |   6     |
|"deleting"           |   7     |
|"awaiting-transfer"  |   8     |
|"error"              |   9     |
|"error_deleting"     |   10    |
|"backing-up"         |   11    |
|"restoring-backup"   |   12    |
|"error_backing-up"   |   13    |
|"error_restoring"    |   14    |
|"error_extending"    |   15    |
|"downloading"        |   16    |
|"uploading"          |   17    |
|"retyping"           |   18    |
|"extending"          |   19    |
