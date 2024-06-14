# Table of Contents
- [Introduction](#introduction)
- [Content](#content)
- [Samples](#sample)

# Introduction <a name="introduction"></a>
This API is used to get static ports assigned to EPGs. Static port binding is a way to associate physical ports on a leaf switch with an EPG.

This allows specific traffic from those ports to be treated according to the policies applied to the EPG.

For more detail information about Cisco ACI REST API, please refer to the following document: https://www.cisco.com/c/en/us/td/docs/switches/datacenter/aci/apic/sw/4-x/rest-api-config/Cisco-APIC-REST-API-Configuration-Guide-411/Cisco-APIC-REST-API-Configuration-Guide-411_chapter_0110.html

# Content <a name="content"></a>
Below REST APIs are used to get static ports used by EPGs.


https://apic-ip-address/api/class/fvCEp.json?query-target=children&target-subtree-class=fvRsCEpToPathEp

# Samples <a name="sample"></a>
<details><summary>API Response</summary>

```json
[        
   {
        "tenant": "NB.BOS",
        "ap": "APP.DEV-AP",
        "epg": "WEB-EPG",
        "cep": "00:50:56:BE:5C:46",
        "pod": "pod-1",
        "node": "node-101",
        "intfname": "pod-1/node-101/Switch101-102_1-ports-45_PolGrp",
        "lcOwn": "local",
        "lcC": "learned,vmm",
        "state": "formed"
    },
    {
        "tenant": "NB.NYC",
        "ap": "L3out-PBR",
        "epg": "L3out-PBR-EPG",
        "cep": "00:50:56:8C:98:49",
        "pod": "pod-2",
        "node": "node-103",
        "intfname": "pod-2/node-103/Switch103-104_1-ports-11_PolGrp",
        "lcOwn": "local",
        "lcC": "vmm",
        "state": "formed"
    },
    //...
]
```
</details>
<br />