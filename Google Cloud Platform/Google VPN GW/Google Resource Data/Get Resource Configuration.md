# Table of Contents
- [Introduction](#introduction)
- [Content](#content)
- [Samples](#sample)

# Introduction <a name="introduction"></a>
The configuration of the Google VPN Gateway is dependent on the Google API response of the Google VPN Gateway as the primary response. The full resource configuration consists of some associated resources' API data, including tunnels.

# Content <a name="content"></a>

Below are the Google APIs used to generate this configuration.

|Resource/Action|Relationship|Google API Version|Google API document|
|------|------|------|------|
| VPN Gateway - Get | self | v1 | https://cloud.google.com/compute/docs/reference/rest/v1/vpnGateways/get
| Tunnels - Get | tunnels | v1 | https://cloud.google.com/compute/docs/reference/rest/v1/vpnTunnels/get https://cloud.google.com/compute/docs/reference/rest/v1/vpnTunnels/list

# Samples <a name="sample"></a>
<details><summary>Configuration File</summary>

```json
{
    "netbrainNotes": "This config file is generated via API",
    "netbrainHostName": "tyler-vpn-000(<vpn_gateway_id>)",
    "kind": "compute#vpnGateway",
    "id": "<vpn_gateway_id>",
    "creationTimestamp": "2021-08-19T12:02:24.423-07:00",
    "name": "tyler-vpn-000",
    "description": "",
    "region": "https://www.googleapis.com/compute/v1/projects/<project-id>/regions/us-east1",
    "network": "https://www.googleapis.com/compute/v1/projects/<project-id>/global/networks/default",
    "selfLink": "https://www.googleapis.com/compute/v1/projects/<project-id>/regions/us-east1/vpnGateways/tyler-vpn-000",
    "labelFingerprint": "xxxxxxxxxxxx",
    "vpnInterfaces": [
        {
            "id": 0,
            "ipAddress": "xx.xx.xx.xx"
        }
    ],
    # vpn tunnels: 
    #   https://cloud.google.com/compute/docs/reference/rest/v1/vpnTunnels/get
    #   https://cloud.google.com/compute/docs/reference/rest/v1/vpnTunnels/list
    "tunnels": [
        {
            "kind": "compute#vpnTunnel",
            "id": "<tunnel-id>",
            "creationTimestamp": "2021-06-14T13:44:43.411-07:00",
            "name": "to-hostproj1-tunnel-1",
            "description": "to-hostproj1-tunnel-1",
            "region": "https://www.googleapis.com/compute/v1/projects/<project-id>/regions/us-west4",
            "vpnGateway": "https://www.googleapis.com/compute/v1/projects/<project-id>/regions/us-west4/vpnGateways/serv-proj2-us-west4-cloudvpn",
            "vpnGatewayInterface": 0,
            "peerGcpGateway": "https://www.googleapis.com/compute/v1/projects/<project-id>/regions/us-west4/vpnGateways/host-proj1-vpc-spk3-cloudvpn",
            "router": "https://www.googleapis.com/compute/v1/projects/<project-id>/regions/us-west4/routers/serv-proj2-us-west4-cloudvpn",
            "peerIp": "xx.xx.xx.xx",
            "sharedSecret": "*",
            "sharedSecretHash": "xxxxxxxxxxxxxxxxxxxxxx",
            "status": "ESTABLISHED",
            "selfLink": "https://www.googleapis.com/compute/v1/projects/<project-id>/regions/us-west4/vpnTunnels/to-hostproj1-tunnel-1",
            "ikeVersion": 2,
            "detailedStatus": "Tunnel is up and running.",
            "localTrafficSelector": [
                "0.0.0.0/0"
            ],
            "remoteTrafficSelector": [
                "0.0.0.0/0"
            ],
            "labelFingerprint": "xxxxxxxxxxx"
        }
    ]
}


```

</details>
<br />