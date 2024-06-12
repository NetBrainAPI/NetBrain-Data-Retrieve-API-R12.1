# Table of Contents
- [Introduction](#introduction)
- [Content](#content)
- [Samples](#sample)

# Introduction <a name="introduction"></a>
This API is used to check status of border switch OSPF Protocol. Status data is essential to ensure the ACI fabric is properly connected to external networks, and confirm the OSPF routes are correctly learned and advertised.

For more detail information about Cisco ACI REST API, please refer to the following document: https://www.cisco.com/c/en/us/td/docs/switches/datacenter/aci/apic/sw/4-x/rest-api-config/Cisco-APIC-REST-API-Configuration-Guide-411/Cisco-APIC-REST-API-Configuration-Guide-411_chapter_0110.html

# Content <a name="content"></a>
Below REST API is used to get status of OSPF Protocol rom Cisco ACI Platform. 


https://apic-ip-address/api/node/mo/<dn>//sys/ospf/inst-default.json/?query-target=subtree&target-subtree-class=ospfAdjEp

# Samples <a name="sample"></a>
<details><summary>API Response</summary>

```json
[
  {
    "ospfAdjEp": {
      "attributes": {
        "area": "0.0.0.103",
        "bdr": "0.0.0.0",
        "bfdSt": "down",
        "dn": "topology/pod-2/node-104/sys/ospf/inst-default/dom-common:default/if-[eth1/21]/adj-20.0.22.200",
        "dr": "0.0.0.0",
        "helloOptions": "2",
        "id": "20.0.22.200",
        "ifId": "0",
        "modTs": "never",
        "monPolDn": "uni/fabric/monfab-default",
        "name": "",
        "operSt": "full",
        "peerIp": "20.0.22.2",
        "peerName": "",
        "prio": "1",
        "status": ""
      }
    }
  },
  {
    "ospfAdjEp": {
      "attributes": {
        "area": "0.0.0.52",
        "bdr": "0.0.0.0",
        "bfdSt": "down",
      }
    }

   }
]
```
</details>
<br />