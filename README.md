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



## OpenStack volumes can be in the following status:
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

## OpenStack server can be in the following status:
openstack_nova_server_status:

|   Status          | Value | Description
|-------------------|-------|--------------------|
| ACTIVE            |   0   |
| BUILD             |   1   | The server has not finished the original build process.
| BUILD(spawning)   |   2   | The server has not finished the original build process but networking works (HP Cloud specific)
| DELETED           |   3   | The server is deleted.
| ERROR             |   4   | The server is in error.
| HARD_REBOOT       |   5   | The server is hard rebooting.
| PASSWORD          |   6   | The password is being reset on the server.
| REBOOT            |   7   | The server is in a soft reboot state.
| REBUILD           |   8   | The server is currently being rebuilt from an image.
| RESCUE            |   9   | The server is in rescue mode.
| RESIZE            |   10  | Server is performing the differential copy of data that changed during its initial copy.
| SHUTOFF           |   11  | The virtual machine (VM) was powered down by the user, but not through the OpenStack Compute API.
| SUSPENDED         |   12  | The server is suspended, either by request or necessity.
| UNKNOWN           |   13  | The state of the server is unknown. Contact your cloud provider.
| VERIFY_RESIZE     |   14  | System is awaiting confirmation that the server is operational after a move or resize.
| MIGRATING         |   15  | The server is migrating. This is caused by a live migration (moving a server that is active) action.
| PAUSED            |   16  | The server is paused.
| REVERT_RESIZE     |   17  | The resize or migration of a server failed for some reason. The destination server is being cleaned up and the original source server is restarting.
| SHELVED           |   18  | The server is in shelved state. Depends on the shelve offload time, the server will be automatically shelved off loaded.
| SHELVED_OFFLOADED |   19  | The shelved server is offloaded (removed from the compute host) and it needs unshelved action to be used again.
| SOFT_DELETED      |   20  | The server is marked as deleted but will remain in the cloud for some configurable amount of time.
