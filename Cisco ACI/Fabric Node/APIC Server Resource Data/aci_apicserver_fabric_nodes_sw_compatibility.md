# Table of Contents
- [Introduction](#introduction)
- [Content](#content)
- [Samples](#sample)

# Introduction <a name="introduction"></a>
This API is sued to check software version compatibility between switches and apic server. Checking and ensuring software version compatibility of fabric nodes is essential for maintaining a stable, secure, and efficient network environment, leveraging new features, and facilitating effective support and maintenance.

For more detail information about Cisco ACI REST API, please refer to the following document: https://www.cisco.com/c/en/us/td/docs/switches/datacenter/aci/apic/sw/4-x/rest-api-config/Cisco-APIC-REST-API-Configuration-Guide-411/Cisco-APIC-REST-API-Configuration-Guide-411_chapter_0110.html

# Content <a name="content"></a>
Below REST API is used to check software version compatibility of Cisco ACI fabric nodes. 


https://apic-ip-address/api/node/class/topSystem.json?&order-by=topSystem.modTs|desc

# Samples <a name="sample"></a>
<details><summary>API Response</summary>

```json
[
    {
        "APIC_Server": "apic1",
        "device_name": "NBLEAF-1",
        "pod": "pod-1",
        "node": "node-101",
        "role": "leaf",
        "version": "n9100-13.1(2g)",
        "compatible": "no"
    },
    {
        "APIC_Server": "apic1",
        "device_name": "NBLEAF-3",
        "pod": "pod-2",
        "node": "node-103",
        "role": "leaf",
        "version": "n9000-14.1(2g)",
        "compatible": "yes"
    },
    //...
]
```
</details>
<br />