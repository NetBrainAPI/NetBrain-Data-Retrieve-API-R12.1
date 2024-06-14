# Table of Contents
- [Introduction](#introduction)
- [Content](#content)
- [Samples](#sample)

# Introduction <a name="introduction"></a>
This API is used to describe interfaces on layer3 Out Border Switches. Checking data of those interfaces is essential for ensuring network connectivity, performance, security, redundancy, and effective policy enforcement. It aids in troubleshooting, maintaining high availability, and supporting network planning and compliance efforts.

For more detail information about Cisco ACI REST API, please refer to the following document: https://www.cisco.com/c/en/us/td/docs/switches/datacenter/aci/apic/sw/4-x/rest-api-config/Cisco-APIC-REST-API-Configuration-Guide-411/Cisco-APIC-REST-API-Configuration-Guide-411_chapter_0110.html

# Content <a name="content"></a>
Below REST API is used to describe interfaces on Layer3 Out Border switches. 


https://apic-ip-address/api/node/class/l3extRsPathL3OutAtt.json?&order-by=l3extRsPathL3OutAtt.modTs|desc

# Samples <a name="sample"></a>
<details><summary>API Response</summary>

```json
[
    {
        "apic": "apic1",
        "pod": "pod-2",
        "node": "node-103",
        "port": "eth1/38",
        "fullname": "pod-2/node-103/eth1/38",
        "portType": "sub-interface"
    },
    {
        "apic": "apic1",
        "pod": "pod-1",
        "node": "node-101",
        "port": "eth1/38",
        "fullname": "pod-1/node-101/eth1/38",
        "portType": "l3-port"
    },
    //...
]
```
</details>
<br />