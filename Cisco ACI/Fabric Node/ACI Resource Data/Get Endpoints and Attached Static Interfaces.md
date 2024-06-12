# Table of Contents
- [Introduction](#introduction)
- [Content](#content)
- [Samples](#sample)

# Introduction <a name="introduction"></a>
This API is used to know which endpoints (such as servers, VMs, and other devices) are connected to the network, and to identify which interfaces endpoints are attached to.

Getting information about endpoints and their attached static interfaces is essential for network management, troubleshooting, security enforcement, performance monitoring, and overall operational efficiency.

For more detail information about Cisco ACI REST API, please refer to the following document: https://www.cisco.com/c/en/us/td/docs/switches/datacenter/aci/apic/sw/4-x/rest-api-config/Cisco-APIC-REST-API-Configuration-Guide-411/Cisco-APIC-REST-API-Configuration-Guide-411_chapter_0110.html

# Content <a name="content"></a>
Below REST API is used. 


https://apic-ip-address/api/node/class/fvRsCEpToPathEp.json?&order-by=fvRsCEpToPathEp.modTs|desc

# Samples <a name="sample"></a>
<details><summary>API Response</summary>

```json
[
    {
        "tenant": "QA_Tenant",
        "ap": "QA_base_app",
        "epg": "QA_FrontServer_EPG",
        "cep": "00:50:56:8C:B8:F7",
        "port": "pod-2/node-104/QA_FrontServer-VPC-7"
    },
    {
        "tenant": "QA_Tenant",
        "ap": "QA_base_app",
        "epg": "QA_FrontServer_EPG",
        "cep": "00:0C:29:D0:BF:5D",
        "port": "pod-2/node-104/QA_FrontServer-VPC-17"
    },

]
```
</details>
<br />