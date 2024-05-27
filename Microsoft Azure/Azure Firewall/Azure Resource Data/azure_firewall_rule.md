# Table of Contents
- [Introduction](#introduction)
- [Content](#content)
- [Samples](#sample)
    - [Sample 1 -- Classic Firewall Rules](#sample-1) 
    - [Sample 2 -- Firewall Rules of Firewall Policies](#sample-2)


# Introduction <a name="introduction"></a>
Passing-in the keyword "firewall_rule" for the param data_type, the API returns the NAT rules, network rules, and applications rules of the Azure Firewall.
There are two types of firewall rules -- classic rules and firewall policy (ref: https://learn.microsoft.com/en-us/azure/firewall/rule-processing).
The classic firewall rules can be found directly in the firewall's Azure API data. The other type of firewall rule can be fetched via firewall policy and its base policy's Azure API data.


# Content <a name="content"></a>
Below are the Azure APIs used to generate this configuration.

|**Resource/Action**|**Relationship**|**Azure API Version**|**Azure API document**|
|------|------|------|------|
| Azure Firewalls - Get | self | 2021-09-01 | https://learn.microsoft.com/en-us/rest/api/firewall/azure-firewalls/get | 
| Firewall Policies - Get | self | 2021-09-01 |   https://learn.microsoft.com/en-us/rest/api/virtualnetwork/firewall-policies/get | 

# Samples <a name="sample"></a>
## Sample 1 -- Classic Firewall Rules <a name="sample-1"></a>

API Response - Classic Firewall Rules

## Sample 2 -- Firewall Rules of Firewall Policies <a name="sample-2"></a>

API Response - Firewall Rules of Firewall Policies

