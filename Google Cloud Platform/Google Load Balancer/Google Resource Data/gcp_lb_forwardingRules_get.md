# Table of Contents
- [Introduction](#introduction-)

# Introduction <a name="introduction"></a>
Google Cloud forwarding rule specifies how to route network traffic to the backend services of a load balancer. 
A forwarding rule includes an IP address, an IP protocol, and one or more ports on which the load balancer accepts traffic .

A forwarding rule and its corresponding IP address represent the frontend configuration of a Google Cloud load balancer .



The API is used to retrieve GCP specified ForwardingRule resource from GCP Platform. 

It leverages the GCP compute engine to fetch details of GCP resources via the GCP RESTful API. 

For a complete list of available API resources for GCP, please refer to the following document: https://cloud.google.com/compute/docs/reference/rest/v1

For API detailed definitions, such as Input, Output, filters, etc., please refer to the following document:
[Google Cloud Observability document](https://cloud.google.com/compute/docs/reference/rest/v1/forwardingRules/get)
