# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Reference](#reference)

# Overview <a name="overview"></a>
Delta vCPU usage for all vCPUs, in vCPU-seconds. To compute the per-vCPU utilization fraction, divide this value by (end-start)*N, where end and start define this value's time interval and N is `compute.googleapis.com/instance/cpu/reserved_cores` at the end of the interval. This value is reported by the hypervisor for the VM and can differ from `agent.googleapis.com/cpu/usage_time`, which is reported from inside the VM.

It leverages the GCP Cloud monitoring to fetch metrics of GCP resources via the GCP RESTful API. 

# Metric Info <a name="metric-info"></a>
* <b>Resource Label Used</b>: The numeric VM instance identifier assigned by Compute Engine (instance_id).
* <b>GCP Original Name</b>: instance/cpu/usage_time

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Define the time range to analyze data points, useful for historical analysis or recent monitoring. Default time range is the last 24 hours.


# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://cloud.google.com/monitoring/api/metrics_gcp
* <b>Metrics API</b>: https://cloud.google.com/monitoring/api/v3/filters