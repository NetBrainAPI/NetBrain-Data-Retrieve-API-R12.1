# Table of Contents
- [Introduction](#introduction)
- [Content](#content)
- [Samples](#sample)

# Introduction <a name="introduction"></a>
This API is used to obtain the status of switch physical interfaces. Monitoring the status of switch physical interfaces is fundamental for maintaining network health, ensuring performance, enhancing security, facilitating troubleshooting, and supporting overall network management and operations.

For more detail information about Cisco ACI REST API, please refer to the following document: https://www.cisco.com/c/en/us/td/docs/switches/datacenter/aci/apic/sw/4-x/rest-api-config/Cisco-APIC-REST-API-Configuration-Guide-411/Cisco-APIC-REST-API-Configuration-Guide-411_chapter_0110.html

# Content <a name="content"></a>
Below REST APIs are used. 


https://apic-ip-address/api/node/class/ethpmPhysIf.json?&order-by=ethpmPhysIf.modTs|desc
https://apic-ip-address/api/node/class/pcAggrIf.json?&order-by=pcAggrIf.modTs|desc
https://apic-ip-address/api/node/class/ethpmAggrIf.json?&order-by=ethpmAggrIf.modTs|desc

# Samples <a name="sample"></a>
<details><summary>API Response</summary>

```json
[
    {
        "pod": "pod-1",
        "node": "node-101",
        "aggr": "",
        "name": "eth1/33",
        "full_name": "pod-1/node-101/eth1/33",
        "member": "",
        "portType": "phy",
        "state": "down",
        "usage": "discovery"
    },
    {
        "pod": "pod-1",
        "node": "node-101",
        "aggr": "",
        "name": "eth1/34",
        "full_name": "pod-1/node-101/eth1/34",
        "member": "",
        "portType": "phy",
        "state": "down",
        "usage": "discovery"
    },
    //...
]
```
</details>
<br />