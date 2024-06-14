# Table of Contents
- [Introduction](#introduction)
- [Content](#content)
- [Samples](#sample)

# Introduction <a name="introduction"></a>
This API is used to describe interfaces on layer2 Out Border Switches. Getting the data of those interfaces is essential for ensuring network connectivity, troubleshooting issues, monitoring performance, maintaining redundancy, verifying configurations, enhancing security, meeting compliance requirements, and gaining operational insights.

For more detail information about Cisco ACI REST API, please refer to the following document: https://www.cisco.com/c/en/us/td/docs/switches/datacenter/aci/apic/sw/4-x/rest-api-config/Cisco-APIC-REST-API-Configuration-Guide-411/Cisco-APIC-REST-API-Configuration-Guide-411_chapter_0110.html

# Content <a name="content"></a>
Below REST API is used to describe interfaces on Layer2 Out Border switches. 


https://apic-ip-address/api/node/class/l2extRsPathL2OutAtt.json?&order-by=l2extRsPathL2OutAtt.modTs|desc

# Samples <a name="sample"></a>
<details><summary>API Response</summary>

```json
[
    {
        "apic": "apic1",
        "pod": "pod-1",
        "node": "node-102",
        "port": "eth1/5",
        "fullname": "pod-1/node-102/eth1/5",
        "portType": ""
    }
]
```
</details>
<br />