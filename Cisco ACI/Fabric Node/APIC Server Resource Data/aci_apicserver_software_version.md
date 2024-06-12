# Table of Contents
- [Introduction](#introduction)
- [Content](#content)
- [Samples](#sample)

# Introduction <a name="introduction"></a>
This API is used to get software version of Cisco ACI fabric nodes (APICs, leaf switches, and spine switches).

The Software Version information can be used to check feature compatibility and interoperability, ensure security, plan upgrade, etc.

For more detail information about Cisco ACI REST API, please refer to the following document: https://www.cisco.com/c/en/us/td/docs/switches/datacenter/aci/apic/sw/4-x/rest-api-config/Cisco-APIC-REST-API-Configuration-Guide-411/Cisco-APIC-REST-API-Configuration-Guide-411_chapter_0110.html

# Content <a name="content"></a>
Below REST API is used to get software version of Cisco ACI fabric nodes. 


https://apic-ip-address/api/node/class/topSystem.json?&order-by=topSystem.modTs|desc

# Samples <a name="sample"></a>
<details><summary>API Response</summary>

```json
[
    {
        "topSystem": {
            "attributes": {
                "address": "10.0.32.64",
                "bootstrapState": "done",
                "controlPlaneMTU": "9000",
                "currentTime": "2024-06-03T20:05:57.498+00:00",
                "dn": "topology/pod-1/node-101/sys",
                "enforceSubnetCheck": "no",
                "etepAddr": "10.10.1.4",
                "fabricDomain": "ACI Fabric1",
                "fabricId": "1",
                "monPolDn": "uni/fabric/monfab-default",
                "name": "NBLEAF-1",
                "nodeType": "unspecified",
                "oobMgmtAddr": "192.168.48.136",
                "role": "leaf",
                "serial": "SAL2012MKCQ",
                "siteId": "1",
                "state": "in-service",
                "systemUpTime": "12:06:38:31.000",
                "tepPool": "10.0.0.0/16",
                "version": "n9000-14.1(2g)",
                "virtualMode": "no"
            }
        }
    },
    {
        "topSystem": {   

        }
    }
]
```
</details>
<br />