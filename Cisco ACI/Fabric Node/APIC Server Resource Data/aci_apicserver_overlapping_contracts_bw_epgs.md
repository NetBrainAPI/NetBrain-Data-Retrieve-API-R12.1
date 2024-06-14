# Table of Contents
- [Introduction](#introduction)
- [Content](#content)
- [Samples](#sample)

# Introduction <a name="introduction"></a>
This API is used to get Overlapping Contracts between EPGs. Overlapping contracts in Cisco ACI occur when multiple contracts apply to the same EPGs, either as providers, consumers, or both.

To get overlapping contracts can help avoid conflicts and ensure efficient network operation.

For more detail information about Cisco ACI REST API, please refer to the following document: https://www.cisco.com/c/en/us/td/docs/switches/datacenter/aci/apic/sw/4-x/rest-api-config/Cisco-APIC-REST-API-Configuration-Guide-411/Cisco-APIC-REST-API-Configuration-Guide-411_chapter_0110.html

# Content <a name="content"></a>
Below REST API is used to get overlapping contracts between EPGs from Cisco ACI Platform. 


https://apic-ip-address/api/node/class/fvCollectionCont.json?rsp-subtree=full

# Samples <a name="sample"></a>
<details><summary>API Response</summary>

```json

[
    {
        "EPG1": "NB.NYC/DC5011/5011Ext-EPG",
        "EPG2": "NB.NYC/NYC.QA/App",
        "Contracts List": "NB.NYC/VZany",
        "Num of Contracts": 1
    },
    {
        "EPG1": "NB.NYC/DC5011/5011Ext-EPG",
        "EPG2": "NB.NYC/DC5011/5011Ext-EPG",
        "Contracts List": "NB.NYC/VZany",
        "Num of Contracts": 1
    },
    {
        "EPG1": "NB.NYC/DC5011/5011Ext-EPG",
        "EPG2": "NB.NYC/L3out-PBR/L3out-PBR-EPG",
        "Contracts List": "NB.NYC/L3out-PBR-Contract",
        "Num of Contracts": 1
    },
    {
        "EPG1": "NB.BOS/APP.QA-AP/BackEnd-EPG",
        "EPG2": "NB.BOS/APP.QA-AP/MiddleWare-EPG",
        "Contracts List": "NB.BOS/l2-197,NB.BOS/QA_backEnd_MiddleWare",
        "Num of Contracts": 2
    },
    //...
]
```
</details>
<br />