# Table of Contents
- [Introduction](#introduction)
- [Content](#content)
- [Samples](#sample)

# Introduction <a name="introduction"></a>
The configuration of the Google Private Service Connect Endpoint relies solely on the corresponding Google API of the globalForwardingRules. The Google API provides detailed information regarding the configuration of the instance, including its IPAddress, serviceDirectoryRegistrations, etc.

# Content <a name="content"></a>
Below are the Google APIs used to generate this configuration.
|Resource/Action|Relationship|Google API Version|Google API document|
|------|------|------|------|
| Cloud Private Service Connect Endpoint - Get | self | v1 | https://cloud.google.com/compute/docs/reference/rest/v1/globalForwardingRules/get

# Samples <a name="sample"></a>
<details><summary>Configuration File</summary>

```json
{
    "netbrainNotes": "This config file is generated via API",
    "netbrainHostName": "psctest1(<psc-id>)",
    "kind": "compute#forwardingRule",
    "id": "<psc-id>",
    "creationTimestamp": "2022-09-08T07:37:00.890-07:00",
    "name": "psctest1",
    "IPAddress": "xx.xx.xx.xx",
    "IPProtocol": "TCP",
    "target": "all-apis",
    "selfLink": "https://www.googleapis.com/compute/v1/projects/<project-id>/global/forwardingRules/psctest1",
    "network": "https://www.googleapis.com/compute/v1/projects/<project-id>/global/networks/central-vpc-hub",
    "serviceDirectoryRegistrations": [
        {
            "namespace": "goog-psc-central-vpc-hub-5165306842222363136",
            "serviceDirectoryRegion": "us-central1"
        }
    ],
    "labelFingerprint": "xxxxxxxxxx",
    "pscConnectionId": "xxxxxxxxxxxxxx"
}
```

</details>
<br />