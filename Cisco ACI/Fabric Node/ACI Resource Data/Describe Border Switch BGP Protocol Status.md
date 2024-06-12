# Table of Contents
- [Introduction](#introduction)
- [Content](#content)
- [Samples](#sample)

# Introduction <a name="introduction"></a>
This API is used to check the EIGRP Protocol status on an ACI border switch. 
Regularly checking EIGRP status is vital for maintaining a robust, secure, and efficient network, ensuring proper routing, diagnosing issues, maintaining security, ensuring high availability, and supporting seamless integration with other network protocols and services.

For more detail information about Cisco ACI REST API, please refer to the following document: https://www.cisco.com/c/en/us/td/docs/switches/datacenter/aci/apic/sw/4-x/rest-api-config/Cisco-APIC-REST-API-Configuration-Guide-411/Cisco-APIC-REST-API-Configuration-Guide-411_chapter_0110.html

# Content <a name="content"></a>
Below REST API is used to get status of EIGRP Protocol rom Cisco ACI Platform. 


https://apic-ip-address/api/mo/<dn>/sys/eigrp.json?query-target=subtree&target-subtree-class=eigrpRoute

# Samples <a name="sample"></a>
<details><summary>API Response</summary>

```json
[
    {
        "eigrpRoute": {
            "attributes": {
                "actStQual": "Local origin",
                "chgQual": "",
                "childAction": "",
                "dn": "topology/pod-1/node-101/sys/eigrp/inst-default/dom-IBNA-1:CASE-A1/af-ipv4-ucast/db-rt/rt-[101.1.101.1/32]",
                "fDist": "128320",
                "flags": "",
                "lastActTs": "2024-05-22T13:27:26.539+00:00",
                "modTs": "never",
                "name": "",
                "operSt": "passive",
                "pfx": "101.1.101.1/32",
                "siaQueryCnt": "0",
                "status": ""
            }
        }
    }
]
```
</details>
<br />