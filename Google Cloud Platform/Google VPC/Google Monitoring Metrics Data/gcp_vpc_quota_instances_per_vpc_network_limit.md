# Table of Contents
- [Introduction](#introduction-)

# Introduction <a name="introduction"></a>
The API is used to retrieve GCP Instances Per VPC Network quota limit . Instance per VPC means The total number of VM instances with a network interface (NIC) in the VPC network of GCP Platform. 

It leverages the GCP Cloud monitoring to fetch metrics of GCP resources via the GCP RESTful API. 



For a complete list of available metrics for each GCP resource, please refer to the following document: https://cloud.google.com/monitoring/api/metrics_gcp

For API detailed definition, please refer to the following document:
[Google Cloud Monitoring document](https://cloud.google.com/monitoring/alerts/using-quota-metrics)