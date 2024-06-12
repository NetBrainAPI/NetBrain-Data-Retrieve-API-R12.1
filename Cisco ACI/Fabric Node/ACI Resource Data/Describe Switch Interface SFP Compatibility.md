# Table of Contents
- [Introduction](#introduction)
- [Content](#content)
- [Samples](#sample)

# Introduction <a name="introduction"></a>
This API is used to check switch interface SFP compatibility. SFP (Small Form-factor Pluggable) modules are interchangeable, hot-swappable components

used in networking equipment to connect fiber optic or copper cables. Interfaces need to be compatible with specific SFP modules to establish proper connections. 

For more detail information about Cisco ACI REST API, please refer to the following document: https://www.cisco.com/c/en/us/td/docs/switches/datacenter/aci/apic/sw/4-x/rest-api-config/Cisco-APIC-REST-API-Configuration-Guide-411/Cisco-APIC-REST-API-Configuration-Guide-411_chapter_0110.html

# Content <a name="content"></a>
Below REST API is used. 


https://apic-ip-address/api/class/<dn>/ethpmFcot.json

# Samples <a name="sample"></a>
<details><summary>API Response</summary>

```json
[
  {
    "ethpmFcot": {
      "attributes": {
        "actualType": "sfp",
        "baseResvd1": "0",
        "baseResvd2": "0",
        "baseResvd3": "0",
        "baseResvd4": "0,0,0",
        "brIn100MHz": "13",
        "brMaxMargin": "0",
        "brMinMargin": "0",
        "ccex": "100",
        "ccid": "160",
        "childAction": "",
        "connectType": "0",
        "dateCode": "49,55,48,55,50,57,32,32",
        "description": "0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0",
        "diagMonType": "0",
        "distIn100mFor9u": "0",
        "distIn10mFor50u": "0",
        "distIn10mFor60u": "0",
        "distIn1mForCu": "100",
        "distInKmFor9u": "0",
        "dn": "topology/pod-1/node-101/sys/phys-[eth1/45]/phys/fcot",
        "encoding": "1",
        "enhOption": "0",
        "extOption": "0,26",
        "fCTxType": "33",
        "fcotNum": "45",
        "fcotStatus": "0",
        "fcotType": "8",
        "flags": "ok",
        "gigEthCC": "8",
        "guiCiscoEID": "unknown",
        "guiCiscoPID": "",
        "guiCiscoPN": "",
        "guiName": "OEM             ",
        "guiPN": "SFPC1110        ",
        "guiRev": "1.0 ",
        "guiSN": "17706510221     ",
        "isFcotPresent": "yes",
        "maxSpeed": "0",
        "minSpeed": "0",
        "modTs": "never",
        "monPolDn": "uni/infra/moninfra-default",
        "partNumber": "0,0,0,0,0,0,0,0,0,0,0",
        "sff8472Compl": "0",
        "state": "inserted",
        "status": "",
        "type": "sfp",
        "typeName": "1000base-T",
        "vendorData": "0,0,17,106,166,230,254,70,184,141,237,76,7,113,206,234,176,169,54,0,0,0,0,0,0,0,0,0,221,163,82,98",
        "vendorId": "0,0,0",
        "vendorName": "79,69,77,32,32,32,32,32,32,32,32,32,32,32,32,32",
        "vendorPn": "83,70,80,67,49,49,49,48,32,32,32,32,32,32,32,32",
        "vendorRev": "49,46,48,32",
        "vendorSn": "49,55,55,48,54,53,49,48,50,50,49,32,32,32,32,32",
        "versionId": "0,0,0,0,0",
        "xcvrCode": "0,0,0,8,0,0,0,0",
        "xcvrExtId": "4",
        "xcvrId": "3"
      }
    }
  },
  {
    "ethpmFcot": {
      "attributes": {
        "actualType": "sfp",
        "baseResvd1": "0",
        "baseResvd2": "0",
        "baseResvd3": "0",
        "baseResvd4": "0,0,0",

      }
    }
  }
]
```
</details>
<br />