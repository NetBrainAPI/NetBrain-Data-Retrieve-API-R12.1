# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [Reference](#reference)

# Overview <a name="overview"></a>
The API is used to retrieve GCP specified Instance resource from GCP Platform. The response includes the details of the instance like Network Interfaces, disk details, CPU details, status, Zone, etc. 

It leverages the GCP compute engine to fetch details of GCP resources via the GCP RESTful API. 

# Metric Info <a name="metric-info"></a>
* <b>GCP Original Name</b>: instances.get

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Define the time range to analyze data points, useful for historical analysis or recent monitoring. Default time range is the last 24 hours.


# Reference <a name="reference"></a>
* For a complete list of available API resources for GCP , please reference to document: https://cloud.google.com/compute/docs/reference/rest/v1

* For API detailed definition, like input, output, field parameters, filters etc., please check Google Cloud Observability document: https://cloud.google.com/compute/docs/reference/rest/v1/instances/get