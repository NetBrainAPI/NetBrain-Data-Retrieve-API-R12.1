# Table of Contents
- [Introduction](#introduction)


# Introduction <a name="introduction"></a>
The API is used to retrieve Azure Virtual Machine Percentage CPU metric data from Azure Platform. 
The metric is the percentage of the allocated compute units that are currently in use by the Virtual Machine(s). 


It leverages the Azure Monitor solution to fetch metrics of Azure resources via the Azure RESTful API. 


For a complete list of available metrics for each Azure resource, please refer to the following document: https://learn.microsoft.com/en-us/azure/azure-monitor/essentials/metrics-supported .


For API detailed definition, such as Input, Output, etc., please refer to the following document:
[Azure Resource Management API](https://learn.microsoft.com/en-us/rest/api/monitor/metrics/list?view=rest-monitor-2023-10-01&tabs=HTTP)