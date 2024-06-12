# Table of Contents
- [Introduction](#introduction)
- [Content](#content)
- [Samples](#sample)

# Introduction <a name="introduction"></a>
This API is used to get all contracts which are consumed by Consumer EPGs. These consumed contracts are the service offered by the provider EPG.

For more detail information about Cisco ACI REST API, please refer to the following document: https://www.cisco.com/c/en/us/td/docs/switches/datacenter/aci/apic/sw/4-x/rest-api-config/Cisco-APIC-REST-API-Configuration-Guide-411/Cisco-APIC-REST-API-Configuration-Guide-411_chapter_0110.html

# Content <a name="content"></a>
Below REST API is used to get consumed contracts by EPGs from Cisco ACI Platform. 


https://apic-ip-address/api/node/class/fvRsCons.json?&order-by=fvRsCons.modTs|desc

# Samples <a name="sample"></a>
<details><summary>API Response</summary>

```json
[
    {
        "consumer_epg": "ASAv/ASAV-PHY/ASAV-PHY-SERVER",
        "cons_contract": "ASAv/ASA-PHY-DIRECT"
    },
    {
        "consumer_epg": "Demo-Lab/Demo/Web",
        "cons_contract": "Demo-Lab/Allow-ICMP"
    },
    {
        "consumer_epg": "QA_MS_Tenant/UntitledAP1/QA_MS_EPG4",
        "cons_contract": "QA_MS_Tenant/QA_MS_Contract"
    },
]
```
</details>
<br />