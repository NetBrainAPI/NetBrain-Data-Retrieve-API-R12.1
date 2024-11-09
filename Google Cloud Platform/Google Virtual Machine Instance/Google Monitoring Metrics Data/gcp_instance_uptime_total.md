# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Reference](#reference)

# Overview <a name="overview"></a>
This API is used to retrieve the elapsed time since the VM was started, in seconds. After sampling, data is not visible for up to 120 seconds. When VM is Stopped (https://cloud.google.com/compute/docs/instances/stop-start-instance#stop-vm-google-cloud), the time is not calculated. On starting the VM again, the timer will reset to 0 for that VM. 

It leverages the GCP Cloud monitoring to fetch metrics of GCP resources via the GCP RESTful API. 

# Metric Info <a name="metric-info"></a>
* <b>Resource Label Used</b>: The numeric VM instance identifier assigned by Compute Engine (instance_id).
* <b>GCP Original Name</b>: instance/uptime_total

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Define the time range to analyze data points, useful for historical analysis or recent monitoring. Default time range is the last 24 hours.


# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://cloud.google.com/monitoring/api/metrics_gcp
* <b>Metrics API</b>: https://cloud.google.com/monitoring/api/v3/filters