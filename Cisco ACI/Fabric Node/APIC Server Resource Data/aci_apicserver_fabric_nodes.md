# Table of Contents
- [Introduction](#introduction)
- [Content](#content)
- [Samples](#sample)

# Introduction <a name="introduction"></a>
This API is used to describe fabric nodes information of Cisco ACI fabric nodes (APICs, leaf switches, and spine switches), such as pod id, node id, device name, IP address, type, model, serial number, etc.

The data can be used for understanding fabric node roles, configurations, and statuses within the network, etc. 

For more detail information about Cisco ACI REST API, please refer to the following document: https://www.cisco.com/c/en/us/td/docs/switches/datacenter/aci/apic/sw/4-x/rest-api-config/Cisco-APIC-REST-API-Configuration-Guide-411/Cisco-APIC-REST-API-Configuration-Guide-411_chapter_0110.html

# Content <a name="content"></a>
Below REST API is used to get Cisco ACI fabric nodes. 


https://apic-ip-address/api/node/class/topSystem.json?&order-by=topSystem.modTs|desc

# Samples <a name="sample"></a>
<details><summary>API Response</summary>

```json
[
    {
        "fabricNode": {
            "attributes": {
                "adSt": "on",
                "address": "10.1.200.66",
                "apicType": "apic",
                "childAction": "",
                "dn": "topology/pod-2/node-104",
                "extMngdBy": "",
                "fabricSt": "active",
                "id": "104",
                "lcOwn": "local",
                "model": "N9K-C9372PX-E",
                "monPolDn": "uni/fabric/monfab-default",
                "name": "NBLEAF-4",
                "nameAlias": "",
                "nodeType": "unspecified",
                "role": "leaf",
                "serial": "FDO222719E4",
                "vendor": "Cisco Systems, Inc",
            }
        }
    },
    {
        "fabricNode": {
            "attributes": {
        ....
            }
        }
   }
]
```
</details>
<br />