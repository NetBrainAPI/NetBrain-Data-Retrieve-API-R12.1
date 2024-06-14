# Table of Contents
- [Introduction](#introduction)
- [Content](#content)
- [Samples](#sample)

# Introduction <a name="introduction"></a>
This API is used to fetch all interfaces status for leaf/spine switches from the APIC server in Cisco ACI, including physical, logical, Layer3 Out Interfaces, etc.

For more detail information about Cisco ACI REST API, please refer to the following document: https://www.cisco.com/c/en/us/td/docs/switches/datacenter/aci/apic/sw/4-x/rest-api-config/Cisco-APIC-REST-API-Configuration-Guide-411/Cisco-APIC-REST-API-Configuration-Guide-411_chapter_0110.html

# Content <a name="content"></a>
Below REST APIs are used to describe all interfaces status.


https://apic-ip-address/api/node/class/ethpmPhysIf.json?&order-by=ethpmPhysIf.modTs|desc
https://apic-ip-address/api/node/class/pcAggrIf.json?&order-by=pcAggrIf.modTs|desc
https://apic-ip-address/api/node/class/ethpmAggrIf.json?&order-by=ethpmAggrIf.modTs|desc  

# Samples <a name="sample"></a>
<details><summary>API Response</summary>

```json
[    
  {
    "device_name": "apic1",
    "pod": "pod-1",
    "node": "node-102",
    "aggr": "",
    "name": "eth1/33",
    "full_name": "pod-1/node-102/eth1/33",
    "portType": "phy",
    "state": "down",
    "usage": "discovery"
  },
  {
    "device_name": "apic1",
    "pod": "pod-1",
    "node": "node-102",
    "aggr": "",
    "name": "eth1/34",
    "full_name": "pod-1/node-102/eth1/34",
    "portType": "phy",
    "state": "down",
    "usage": "discovery"
  },     //...
]
```
</details>
<br />