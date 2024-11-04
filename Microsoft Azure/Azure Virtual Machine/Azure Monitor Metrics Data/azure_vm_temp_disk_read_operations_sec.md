# Table of Contents
- [Introduction](#introduction)


# Introduction <a name="introduction"></a>
The API is used to retrieve Azure Virtual Machine Temp Disk Read Operations/Sec metric data from Azure API Server (https://management.azure.com/). This metric is about read IOPS from a single disk during monitoring period for Temp Disk.



It leverages the Azure Monitor solution to fetch metrics of Azure resources via the Azure RESTful API. The original Azure monitor metrics name: Temp Disk Read Operations/Sec



For a complete list of available metrics for each Azure resource, please reference to Microsoft document: https://learn.microsoft.com/en-us/azure/azure-monitor/essentials/metrics-supported 

For Temp Disk Read Operations/Sec metric detailed information, please refer to Microsoft document: https://learn.microsoft.com/en-us/azure/azure-monitor/reference/supported-metrics/microsoft-compute-virtualmachines-metrics

For Azure Metrics APIs detailed definition, such as Input, Output, etc., please refer to the following document:
[Microsoft Azure Resource Management API document](https://learn.microsoft.com/en-us/rest/api/monitor/metrics/list?view=rest-monitor-2023-10-01&tabs=HTTP)
