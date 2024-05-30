# Table of Contents
- [Introduction](#introduction)


# Introduction <a name="introduction"></a>
Google Cloud routes define the paths that network traffic takes from a virtual machine (VM) instance to other destinations. 
These destinations can be inside your Google Cloud Virtual Private Cloud (VPC) network (for example, in another VM) or outside it.

In a VPC network, a route consists of a single destination prefix in CIDR format and a single next hop.


The API is used to retrieve GCP specified Route resource from GCP Platform. The response include the details of the routes such as network URL, route type, details of next-hop, etc.

It leverages the GCP compute engine to fetch details of GCP resources via the GCP RESTful API. 


For a complete list of available API resources for GCP, please refer to the following document: https://cloud.google.com/compute/docs/reference/rest/v1


For API detailed definitions, such as input, output, filters, etc., please refer to the following document:
[Google Cloud Observability ](https://cloud.google.com/compute/docs/reference/rest/v1/routes/get)