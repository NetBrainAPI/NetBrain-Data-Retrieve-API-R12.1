# Table of Contents
- [Introduction](#introduction)


# Introduction <a name="introduction"></a>
The API is used to retrieve Azure Application Gateway AvgRequestCountPerHealthyHost metric data from Azure API Server (https://management.azure.com/). The metric is about average request count per minute per healthy backend host in a pool. 



It leverages the Azure Monitor solution to fetch metrics of Azure resources via the Azure RESTful API. The original Azure monitor metrics name: AvgRequestCountPerHealthyHost



For a complete list of available metrics for each Azure resource, please reference to Microsoft document: https://learn.microsoft.com/en-us/azure/azure-monitor/essentials/metrics-supported

For AvgRequestCountPerHealthyHost metric detailed information, please refer to Microsoft document: https://learn.microsoft.com/en-us/azure/azure-monitor/reference/supported-metrics/microsoft-network-applicationgateways-metrics

For API detailed definition, such as input, output, etc., please refer to the following document:
[Azure Resource Management API document](https://learn.microsoft.com/en-us/rest/api/monitor/metrics/list?view=rest-monitor-2023-10-01&tabs=HTTP)