# Table of Contents
- [Introduction](#introduction)
- [API Definition](#api_def)
    - [Input Parameters](#input)
    - [Output](#output)
- [Special Notes](#special_notes)
    - [ExpressRoute Circuit](#circuit)
    - [Virtual Network](#vnet)
- [Samples](#sample)   


# Introduction <a name="introduction"></a>
The metric indicates the overall health of this firewall. The Unit is Percent. The Aggregation Type is Average. Time Grains (Intervals at which the metric is sampled) is PT1M(Every 1 minute).

Document: https://learn.microsoft.com/en-us/azure/azure-monitor/reference/supported-metrics/microsoft-network-azurefirewalls-metrics

# API Definition <a name="api_def"></a>
```python

```

## Input Parameters <a name="input"></a>
Copied from other API, draft
 - `api_server_id`(str) - The Azure Tenant API Server Instance ID saved in Device.
 - `azure_resource_uri`(str) - The resource identifier for the Azure resource whose metrics are to be fetched.
 - `params`(dic) - A dictionary containing additional URL parameters to use when calling the Azure monitor metrics API. For a complete list of available metrics for each Azure resource, please reference to Microsoft document: https://learn.microsoft.com/en-us/azure/azure-monitor/essentials/metrics-supported .
 - `api_version[optional]`(str) - The API version to use for the Azure monitor metrics API.

## Output <a name="output"></a>
Copied from other API, draft

> resp_body_json: The JSON response body of the HTTP request to the Azure monitor metrics API. This is a dictionary with string keys and values.

# Special Notes <a name="special_notes"></a>
Copied from other API, draft

## ExpressRoute Circuit <a name="circuit"></a>
 - In NetBrain, we generate two MSEE (Microsoft Enterprise Edge) devices (Primary and Secondary) for each Azure ExpressRoute Circuit. 
 - The Azure ExpressRoute Circuit resource URI is saved in the "circuitId" data field of MSEE.
 - For the usage please check samples below.

## Virtual Network <a name="vnet"></a>
 - In NetBrain, we generate an "Azure VNet Distributed Router" for each Azure Virtual Network to represent its networking entity.
 - The Azure Virtual Network's resource URI is saved in the "vNetId" data field of the Azure VNet Distributed Router.
 - For the usage please check samples below.

# Samples <a name="sample"></a>
```python
'''
	   {
      "key": "azure_firewall_health",
      "displayName": "Azure Firewall FirewallHealth",
      "description": "Azure Firewall FirewallHealth",
      "categoryKey": "azure_monitor_metrics",
      "isBuiltin": true,
      "apiDef": {
        "retrieveData": {
          "api": "NBAzureParserAPILibrary.GetMetrics",
          "apiParamsValue": {
            "START_TIME": {
              "unit": "hours",
              "value": 3
            },
            "END_TIME": {
              "unit": "days",
              "value": 0
            },
            "METRIC_NAME": "FirewallHealth"
          }
        }
      }
'''

