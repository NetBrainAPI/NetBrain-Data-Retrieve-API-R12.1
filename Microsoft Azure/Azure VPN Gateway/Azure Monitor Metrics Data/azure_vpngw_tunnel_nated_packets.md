# Table of Contents
- [Introduction](#introduction)


# Introduction <a name="introduction"></a>
The API is used to retrieve Azure VPN Gateway TunnelNatedPackets metric data from Azure API Server (https://management.azure.com/). This metric is about number of packets that were NATed on a tunnel by a NAT rule.



It leverages the Azure Monitor solution to fetch metrics of Azure resources via the Azure RESTful API. The original Azure monitor metrics name: TunnelNatedPackets



For a complete list of available metrics for each Azure resource, please reference to Microsoft document: https://learn.microsoft.com/en-us/azure/azure-monitor/essentials/metrics-supported 

For TunnelNatedPackets metric detailed information, please refer to Microsoft document: https://learn.microsoft.com/en-us/azure/azure-monitor/reference/supported-metrics/microsoft-network-vpngateways-metrics

For API detailed definition, such as input, output, etc., please refer to the following document:
[Azure Resource Management API document](https://learn.microsoft.com/en-us/rest/api/monitor/metrics/list?view=rest-monitor-2023-10-01&tabs=HTTP)