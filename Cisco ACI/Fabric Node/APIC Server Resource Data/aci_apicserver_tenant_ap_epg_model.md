# Table of Contents
- [Introduction](#introduction)
- [Content](#content)
- [Sample](#sample)



# Introduction <a name="introduction"></a>
This API is used to describe ACI fundamental components by a logical network model including Tenants, APs, EPGs, and Endpoints. 
The data model has four keys including values of Tenant, AP, EPG, and Endpoint respectively. 

This API can be used to diagnose Cisco ACI network configurations, such as to check an EPG without any endpoint, etc.

For more details about Cisco ACI REST API, please refer to the following document: https://www.cisco.com/c/en/us/td/docs/switches/datacenter/aci/apic/sw/4-x/rest-api-config/Cisco-APIC-REST-API-Configuration-Guide-411/Cisco-APIC-REST-API-Configuration-Guide-411_chapter_0110.html


# Content <a name="content"></a>
Below REST API is used to get fundamental components from Cisco ACI Platform. 

https://apic-ip-address/api/class/fvTenant.json?query-target=subtree&target-subtree-class=fvAp,fvAEPg,fvCEp


# Sample <a name="sample"></a>
API Response - Cisco ACI Tenant AP EPG Model

```json
[
    {
        "tenant": "NB.BOS",
        "ap": "APP.QA-AP",
        "epg": "BackEnd-EPG",
        "cep": ""
    },
    {
        "tenant": "NB.BOS",
        "ap": "APP.QA-AP",
        "epg": "MiddleWare-EPG",
        "cep": ""
    },
    {
        "tenant": "NB.BOS",
        "ap": "APP.QA-AP",
        "epg": "TestTabooEPG",
        "cep": ""
    },
    {
        "tenant": "Demo-Lab",
        "ap": "Demo-PBR",
        "epg": "WEB",
        "cep": "00:50:56:BE:40:C1"
    },     ....
]
```