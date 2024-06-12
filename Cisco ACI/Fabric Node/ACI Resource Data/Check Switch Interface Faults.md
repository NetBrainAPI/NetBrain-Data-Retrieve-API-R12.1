# Table of Contents
- [Introduction](#introduction)
- [Content](#content)
- [Samples](#sample)

# Introduction <a name="introduction"></a>
This API is used to check if there is any switch interface faults. To get interface faults alert is essential for ensuring the smooth operation security, and reliability of your network infrastructure.

For more detail information about Cisco ACI REST API, please refer to the following document: https://www.cisco.com/c/en/us/td/docs/switches/datacenter/aci/apic/sw/4-x/rest-api-config/Cisco-APIC-REST-API-Configuration-Guide-411/Cisco-APIC-REST-API-Configuration-Guide-411_chapter_0110.html

# Content <a name="content"></a>
Below REST API is used. 


https://apic-ip-address/api/mo/<node_dn>/sys.json

# Samples <a name="sample"></a>
<details><summary>API Response</summary>

```json
[    
 {
  "intf": "Vlan170",
  "intf_status": "Up",
  "bandwidth": 10000000,
  "traffic_in_byte": 0,
  "traffic_out_byte": 0,
  "used64couter": false,
  "link_error_in": 0,
  "link_error_out": 0,
  "crc_error": 0,
  "collisions": 0,
  "dropEvents": 0,
  "rXNoErrors": 0,
  "tXNoErrors": 0,
  "sys_uptime": 673257500
 }
]
```
</details>
<br />