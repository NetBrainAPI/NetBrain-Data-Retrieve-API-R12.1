# Table of Contents
- [Introduction](#introduction)


# Introduction <a name="introduction"></a>
The API is used to retrieve Azure Application Gateway BackendFirstByteResponseTime metric data from Azure API Server (https://management.azure.com/). The metric is about time interval between start of establishing a connection to backend server and receiving the first byte of the response header, approximating processing time of backend server. 



It leverages the Azure Monitor solution to fetch metrics of Azure resources via the Azure RESTful API. The original Azure monitor metrics name: BackendFirstByteResponseTime



For a complete list of available metrics for each Azure resource, please reference to Microsoft document: https://learn.microsoft.com/en-us/azure/azure-monitor/essentials/metrics-supported

For BackendFirstByteResponseTime metric detailed information, please refer to Microsoft document: https://learn.microsoft.com/en-us/azure/azure-monitor/reference/supported-metrics/microsoft-network-applicationgateways-metrics

For API detailed definition, such as input, output, etc., please refer to the following document:
[Azure Resource Management API document](https://learn.microsoft.com/en-us/rest/api/monitor/metrics/list?view=rest-monitor-2023-10-01&tabs=HTTP)
