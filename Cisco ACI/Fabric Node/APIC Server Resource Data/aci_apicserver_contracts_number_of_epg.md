# Table of Contents
- [Introduction](#introduction)
- [Content](#content)
- [Sample](#sample)



# Introduction <a name="introduction"></a>
This API is used to retrieve number of contracts of Provider EPGs. Each EPG can consume and provide a certain number of contracts.

The specific limits depend on the hardware and software versions.

For more detail information about Cisco ACI REST API, please refer to the following document: https://www.cisco.com/c/en/us/td/docs/switches/datacenter/aci/apic/sw/4-x/rest-api-config/Cisco-APIC-REST-API-Configuration-Guide-411/Cisco-APIC-REST-API-Configuration-Guide-411_chapter_0110.html


# Content <a name="content"></a>
Below REST API is used to get consumed contracts by EPGs from Cisco ACI Platform. 


https://apic-ip-address/api/node/class/fvRsProv.json?&order-by=fvRsProv.modTs|desc



# Sample <a name="sample"></a>
<details><summary>API Response</summary>

```json
[   
    {
        "Provider EPG": "QA_MS_Tenant/UntitledAP1/QA_MS_EPG4",
        "Contract list": [
            "QA_MS_Tenant/QA_MS_Contract"
        ],
        "Num of Contracts": 1
    },
    {
        "Provider EPG": "QA_MS_Tenant/UntitledAP1/QA_MS_EPG3",
        "Contract list": [
            "QA_MS_Tenant/QA_MS_Contract"
        ],
        "Num of Contracts": 1
    },
    {
        "Provider EPG": "IBNA-1/Case-A1/Provider",
        "Contract list": [
            "IBNA-1/Contract9",
            "IBNA-1/Contract8",
            "IBNA-1/Contract7",
            "IBNA-1/Contract6",
            "IBNA-1/Contract5",
            "IBNA-1/Contract4",
            "IBNA-1/Contract24",
            "IBNA-1/Contract23",
            "IBNA-1/Contract22",
            "IBNA-1/Contract21",
            "IBNA-1/Contract20",
            "IBNA-1/Contract19",
            "IBNA-1/Contract18",
            "IBNA-1/Contract17",
            "IBNA-1/Contract16",
            "IBNA-1/Contract15",
            "IBNA-1/Contract14",
            "IBNA-1/Contract13",
            "IBNA-1/Contract12",
            "IBNA-1/Contract11",
            "IBNA-1/Contract3",
            "IBNA-1/Contract2",
            "IBNA-1/Contract1"
        ],
        "Num of Contracts": 23
    }

]
```