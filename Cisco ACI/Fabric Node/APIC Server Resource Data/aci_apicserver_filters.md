# Table of Contents
- [Introduction](#introduction)
- [Content](#content)
- [Samples](#sample)

# Introduction <a name="introduction"></a>
This API is used to get filters which are applied to endpoint groups (EPGs) and contracts to control the communication between different EPGs.

Filters can be based on various attributes such as IP addresses, MAC addresses, TCP/UDP ports, VLAN tags, or even application profiles.

For more detail information about Cisco ACI REST API, please refer to the following document: https://www.cisco.com/c/en/us/td/docs/switches/datacenter/aci/apic/sw/4-x/rest-api-config/Cisco-APIC-REST-API-Configuration-Guide-411/Cisco-APIC-REST-API-Configuration-Guide-411_chapter_0110.html

# Content <a name="content"></a>
Below REST API is used to get filters from Cisco ACI Platform. 


https://apic-ip-address//api/node/class/fvRsProv.json?&order-by=fvRsProv.modTs|desc

# Samples <a name="sample"></a>
<details><summary>API Response</summary>

```json
[     
    {
        "provider_epg": "ASAv/ASAV-PHY/ASAV-PHY-CLIENT",
        "prov_contract": "ASAv/ASA-PHY-DIRECT"
    },
    {
        "provider_epg": "Demo-Lab/Demo/DB",
        "prov_contract": "Demo-Lab/Allow-ICMP"
    },
    {
        "provider_epg": "QA_MS_Tenant/UntitledAP1/QA_MS_EPG4",
        "prov_contract": "QA_MS_Tenant/QA_MS_Contract"
    },    
]
```
</details>
<br />