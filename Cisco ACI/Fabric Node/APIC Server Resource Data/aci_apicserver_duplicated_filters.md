# Table of Contents
- [Introduction](#introduction)
- [Content](#content)
- [Samples](#sample)

# Introduction <a name="introduction"></a>
This API is used to identify ACI duplicated filters with different name but same contents. Duplicates can cause confusion, inefficiency, and potential security issues. Check Duplicated Filters.

For more detail information about Cisco ACI REST API, please refer to the following document: https://www.cisco.com/c/en/us/td/docs/switches/datacenter/aci/apic/sw/4-x/rest-api-config/Cisco-APIC-REST-API-Configuration-Guide-411/Cisco-APIC-REST-API-Configuration-Guide-411_chapter_0110.html

# Content <a name="content"></a>
Below REST API is used to get filters from Cisco ACI Platform. 


https://apic-ip-address/api/node/class/vzEntry.json?&order-by=vzEntry.modTs|desc

# Samples <a name="sample"></a>
<details><summary>API Response</summary>

```json
[         
    {
        "tenant": "ASAv",
        "filter_list": [
            "ASAv/ASA-PHY-ANY_Filter",
            "ASAv/ASAv37-ICMP-Filter",
            "ASAv/ASAv-39_Filter",
            "ASAv/ASAv38_Filter",
            "ASAv/ASAv42_Filter",
            "ASAv/permit-ICMP"
        ],
        "content": "no|unspecified|ip|icmp||unspecified|unspecified|unspecified|",
        "filters_number": 6
    },
    {
        "tenant": "ASAv",
        "filter_list": [
            "ASAv/ASAv43-OneArm_Filter",
            "ASAv/ANY_Filter",
            "ASAv/Paloalto-Onearm_Filter",
            "ASAv/All_IP"
        ],
        "content": "no|unspecified|ip|unspecified||unspecified|unspecified|unspecified|",
        "filters_number": 4
    },    
    //...
]
```
</details>
<br />