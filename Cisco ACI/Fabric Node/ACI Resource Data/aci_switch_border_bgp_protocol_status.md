# Table of Contents
- [Introduction](#introduction)
- [Content](#content)
- [Samples](#sample)

# Introduction <a name="introduction"></a>
Border switches (also known as border leaf switches) are responsible for connecting the ACI fabric to external networks.

This API is used to check the status of BGP neighbors to ensure that they are established and exchanging routes.

For more detail information about Cisco ACI REST API, please refer to the following document: https://www.cisco.com/c/en/us/td/docs/switches/datacenter/aci/apic/sw/4-x/rest-api-config/Cisco-APIC-REST-API-Configuration-Guide-411/Cisco-APIC-REST-API-Configuration-Guide-411_chapter_0110.html

# Content <a name="content"></a>
Below REST API is used to get status of BGP Protocol rom Cisco ACI Platform. 


https://apic-ip-address/api/node/mo/<dn>/sys/bgp/inst.json?query-target=subtree&target-subtree-class=bgpPeerEntry

# Samples <a name="sample"></a>
<details><summary>API Response</summary>

```json
[
    {
        "bgpPeerEntry": {
            "attributes": {
                "addr": "10.1.8.65",
                "connAttempts": "63997",
                "dn": "topology/pod-2/node-104/sys/bgp/inst/dom-overlay-1/peer-[10.1.8.65/32]/ent-[10.1.8.65]",
                "fd": "4294967295",
                "flags": "cap-neg,gr-enabled",
                "holdIntvl": "180",
                "kaIntvl": "60",
                "lastFlapTs": "2024-03-18T22:44:05.672+00:00",
                "localIp": "0.0.0.0",
                "localPort": "unspecified",
                "modTs": "never",
                "monPolDn": "uni/fabric/monfab-default",
                "name": "",
                "operSt": "idle",
                "passwdSet": "disabled",
                "peerIdx": "1",
                "prevOperSt": "idle",
                "rcvCap": "",
                "remotePort": "unspecified",
                "rtrId": "0.0.0.0",
                "shutStQual": "unspecified",
                "stReason": "none",
                "status": "",
                "type": "ibgp",
            }
        }
    },
    {
        "bgpPeerEntry": {
            "attributes": {
                "addr": "10.1.200.65",    
                 //....
            }
        }
    }
]
```
</details>
<br />