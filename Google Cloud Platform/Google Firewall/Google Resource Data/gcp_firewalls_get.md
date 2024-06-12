# Table of Contents
- [Introduction](#introduction-)

# Introduction <a name="introduction"></a>
VPC firewall rules let you allow or deny connections to or from virtual machine (VM) instances in your VPC network. 

You can think of the VPC firewall rules as existing not only between your instances and other networks, but also between individual instances within the same network

The API is used to retrieve GCP specified Firewall resource from GCP Platform. The response include the details of the firewall such as name, network, source, destination, etc.



It leverages the GCP compute engine to fetch details of GCP resources via the GCP RESTful API. 

For a complete list of available API resources for GCP, please refer to the following document: https://cloud.google.com/compute/docs/reference/rest/v1

For API detailed definitions, such as Input, Output, filters, etc., please refer to the following document:
[Google Cloud Observability document](https://cloud.google.com/compute/docs/reference/rest/v1/firewalls/get)