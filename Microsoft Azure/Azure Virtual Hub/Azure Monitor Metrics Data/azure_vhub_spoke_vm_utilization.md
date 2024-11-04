# Table of Contents
- [Introduction](#introduction)


# Introduction <a name="introduction"></a>
The API is used to retrieve Azure Virtual Hub SpokeVMUtilization metric data from Azure API Server (https://management.azure.com/). The metric is about number of deployed spoke VMs as a percentage of the total number of spoke VMs that the hub's routing infrastructure units can support.



It leverages the Azure Monitor solution to fetch metrics of Azure resources via the Azure RESTful API. The original Azure monitor metrics name: SpokeVMUtilization



For a complete list of available metrics for each Azure resource, please reference to Microsoft document: https://learn.microsoft.com/en-us/azure/azure-monitor/essentials/metrics-supported

For SpokeVMUtilization metric detailed information, please refer to Microsoft document: https://learn.microsoft.com/en-us/azure/azure-monitor/reference/supported-metrics/microsoft-network-virtualhubs-metrics

For Azure Metrics APIs detailed definition, such as Input, Output, etc., please refer to the following document:
[Microsoft Azure Resource Management API document](https://learn.microsoft.com/en-us/rest/api/monitor/metrics/list?view=rest-monitor-2023-10-01&tabs=HTTP)
