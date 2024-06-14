# Table of Contents
- [Introduction](#introduction)
- [Content](#content)
- [Samples](#sample)

# Introduction <a name="introduction"></a>
This API is used to get static ports on EPGs. EPG can be associated with static ports to ensure specific physical ports on a switch are directly tied to an EPG.

For more detail information about Cisco ACI REST API, please refer to the following document: https://www.cisco.com/c/en/us/td/docs/switches/datacenter/aci/apic/sw/4-x/rest-api-config/Cisco-APIC-REST-API-Configuration-Guide-411/Cisco-APIC-REST-API-Configuration-Guide-411_chapter_0110.html

# Content <a name="content"></a>
Below REST APIs are used to get static ports attached to EPGs.


https://apic-ip-address/api/node/class/fvRsPathAtt.json?&order-by=fvRsPathAtt.modTs|desc

# Samples <a name="sample"></a>
<details><summary>API Response</summary>

```json
[        
    {
        "apicServer": "apic1",
        "tenant": "QA_Tenant",
        "ap": "QA_base_app",
        "epg": "QA_FrontServer_EPG",
        "pod": "pod-1",
        "node": "node-101",
        "port": "pod-1/node-101/eth1/13",
        "encap": "vlan-2000",
        "mode": "untagged",
        "instrImedcy": "lazy",
        "state": "unformed"
    },
    {
        "apicServer": "apic1",
        "tenant": "NB.NSX",
        "ap": "NSX-EPG",
        "epg": "NSX-SITEA-EPG3-724",
        "pod": "pod-2",
        "node": "node-104",
        "port": "pod-2/node-104/eth1/24",
        "encap": "vlan-724",
        "mode": "native",
        "instrImedcy": "lazy",
        "state": "unformed"
    },    
    //...
]
```
</details>
<br />