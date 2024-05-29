# Table of Contents
- [Introduction](#introduction)
- [Content](#content)
- [Samples](#sample)

# Introduction <a name="introduction"></a>
The configuration of the Google Load Balancer is dependent on the Google API response of the Forwarding Rules as the primary response. There is no distinct between internal or external, Layer 4 or Layer 7, and each load balance is the combination of various resources. The full resource configuration consists of some associated resources' API data, including backendService, group. 

# Content <a name="content"></a>
Below are the Google APIs used to generate this configuration.
|Resource/Action|Relationship|Google API Version|Google API document|
|------|------|------|------|
| Load Balancers - Get | self | v1 | https://cloud.google.com/compute/docs/reference/rest/v1/forwardingRules/get
| Target HTTP Proxies - Get | target | v1 | https://cloud.google.com/compute/docs/reference/rest/v1/targetHttpProxies/get
| Url Map - Get | target.urlMap | v1 | https://cloud.google.com/compute/docs/reference/rest/v1/regionUrlMaps/get
| Default Service - Get | target.urlMap.pathMatchers.defaultService | v1 | https://cloud.google.com/compute/docs/reference/rest/v1/backendServices/get
| Service - Get | target.urlMap.pathMatchers.pathRules.service | v1 | https://cloud.Default.com/compute/docs/reference/rest/v1/backendServices/get
| Default Service - Get | target.urlMap.defaultService | v1 | https://cloud.google.com/compute/docs/reference/rest/v1/backendServices/get
| Backend Service - Get | backendService | v1 | https://cloud.google.com/compute/docs/reference/rest/v1/backendServices/get
| Instance Groups - Get | backendService.backends.group | v1 | https://cloud.google.com/compute/docs/reference/rest/v1/instanceGroups/get

# Samples <a name="sample"></a>
<details><summary>Configuration File</summary>

```json
{
    "netbrainNotes": "This config file is generated via API",
    "netbrainHostName": "host-proj2-tcp-internal-lb1(<ldb_id>-internal-tcp-loadbalancer)",
    "kind": "compute#forwardingRule",
    "id": "<ldb_id>",
    "creationTimestamp": "2021-07-15T18:35:38.345-07:00",
    "name": "host-proj2-tcp-internal-lb1-frontend",
    "description": "",
    "region": "https://www.googleapis.com/compute/v1/projects/<project-id>/regions/us-central1",
    "IPAddress": "xx.xx.xx.xx",
    "IPProtocol": "TCP",
    "portRange": "80-80",
    # Target: https://cloud.google.com/compute/docs/reference/rest/v1/targetHttpProxies/get
    "target": {
        "kind": "compute#targetHttpProxy",
        "id": "3267693297597854555",
        "creationTimestamp": "2021-05-05T14:27:16.252-07:00",
        "name": "lb5-http-internal-lb-target-proxy",
        "selfLink": "https://www.googleapis.com/compute/v1/projects/<project-id>/regions/us-east1/targetHttpProxies/lb5-http-internal-lb-target-proxy",
        # UrlMap: https://cloud.google.com/compute/docs/reference/rest/v1/regionUrlMaps/get
        "urlMap": {
            "kind": "compute#urlMap",
            "id": "<url-map-id>",
            "creationTimestamp": "2021-05-05T14:27:12.247-07:00",
            "name": "lb5-http-internal-lb",
            "selfLink": "https://www.googleapis.com/compute/v1/projects/<project-id>/regions/us-east1/urlMaps/lb5-http-internal-lb",
            "hostRules": [
                {
                    "hosts": [
                        "<hostname>"
                    ],
                    "pathMatcher": "path-matcher-1"
                }
            ],
            "pathMatchers": [
                {
                    "name": "path-matcher-1",
                    # BackendService: https://cloud.google.com/compute/docs/reference/rest/v1/backendServices/get
                    "defaultService": {
                        "kind": "compute#backendService",
                        "id": "<default-service-id>",
                        "creationTimestamp": "2021-05-05T14:26:55.156-07:00",
                        "name": "lb5-http-internal-lb-backend",
                        "description": "",
                        "selfLink": "https://www.googleapis.com/compute/v1/projects/<project-id>/regions/us-east1/backendServices/lb5-http-internal-lb-backend",
                        "backends": [
                            {
                                "description": "",
                                "group": "https://www.googleapis.com/compute/v1/projects/<project-id>/regions/us-east1/instanceGroups/traffic-director-ig",
                                "balancingMode": "UTILIZATION",
                                "maxUtilization": 0.8,
                                "capacityScaler": 1
                            }
                        ],
                        "healthChecks": [
                            "https://www.googleapis.com/compute/v1/projects/<project-id>/regions/us-east1/healthChecks/lb5-http-internal-lb-health-check"
                        ],
                        "timeoutSec": 30,
                        "port": 80,
                        "protocol": "HTTP",
                        "fingerprint": "xxxxxxxx",
                        "portName": "http",
                        "sessionAffinity": "NONE",
                        "affinityCookieTtlSec": 0,
                        "region": "https://www.googleapis.com/compute/v1/projects/<project-id>/regions/us-east1",
                        "loadBalancingScheme": "INTERNAL_MANAGED",
                        "connectionDraining": {
                            "drainingTimeoutSec": 300
                        },
                        "logConfig": {
                            "enable": false,
                            "optionalMode": "EXCLUDE_ALL_OPTIONAL"
                        },
                        "localityLbPolicy": "ROUND_ROBIN"
                    },
                    "pathRules": [
                         {
                            # BackendService: https://cloud.google.com/compute/docs/reference/rest/v1/backendServices/get
                            "service": {
                                "kind": "compute#backendService",
                                "id": "<backend-service-id>",
                                "creationTimestamp": "2021-05-05T14:34:50.741-07:00",
                                "name": "lb4-http-internal-lb-backend",
                                "description": "",
                                "selfLink": "https://www.googleapis.com/compute/v1/projects/<project-id>9/regions/us-east1/backendServices/lb4-http-internal-lb-backend",
                                "backends": [
                                    {
                                        "description": "",
                                        "group": "https://www.googleapis.com/compute/v1/projects/<project-id>9/regions/us-east1/instanceGroups/lb5-http-internal-lb-instance-group",
                                        "balancingMode": "UTILIZATION",
                                        "maxUtilization": 0.8,
                                        "capacityScaler": 1
                                    }
                                ],
                                "healthChecks": [
                                    "https://www.googleapis.com/compute/v1/projects/<project-id>9/regions/us-east1/healthChecks/lb4-http-internal-lb-health-check"
                                ],
                                "timeoutSec": 30,
                                "port": 80,
                                "protocol": "HTTP",
                                "fingerprint": "xxxxxxxxxxxx",
                                "portName": "http",
                                "sessionAffinity": "NONE",
                                "affinityCookieTtlSec": 0,
                                "region": "https://www.googleapis.com/compute/v1/projects/<project-id>9/regions/us-east1",
                                "loadBalancingScheme": "INTERNAL_MANAGED",
                                "connectionDraining": {
                                    "drainingTimeoutSec": 300
                                },
                                "logConfig": {
                                    "enable": false,
                                    "optionalMode": "EXCLUDE_ALL_OPTIONAL"
                                },
                                "localityLbPolicy": "ROUND_ROBIN"
                            },
                            "paths": [
                                "/image"
                            ]
                        }
                    ]
                }
            ],
            # BackendService: https://cloud.google.com/compute/docs/reference/rest/v1/backendServices/get
            "defaultService": {
                "kind": "compute#backendService",
                "id": "<default-service-id>",
                "creationTimestamp": "2021-05-05T14:26:55.156-07:00",
                "name": "lb5-http-internal-lb-backend",
                "description": "",
                "selfLink": "https://www.googleapis.com/compute/v1/projects/<project-id>/regions/us-east1/backendServices/lb5-http-internal-lb-backend",
                "backends": [
                    {
                        "description": "",
                        "group": "https://www.googleapis.com/compute/v1/projects/<project-id>/regions/us-east1/instanceGroups/traffic-director-ig",
                        "balancingMode": "UTILIZATION",
                        "maxUtilization": 0.8,
                        "capacityScaler": 1
                    }
                ],
                "healthChecks": [
                    "https://www.googleapis.com/compute/v1/projects/<project-id>/regions/us-east1/healthChecks/lb5-http-internal-lb-health-check"
                ],
                "timeoutSec": 30,
                "port": 80,
                "protocol": "HTTP",
                "fingerprint": "xxxxxxx",
                "portName": "http",
                "sessionAffinity": "NONE",
                "affinityCookieTtlSec": 0,
                "region": "https://www.googleapis.com/compute/v1/projects/<project-id>/regions/us-east1",
                "loadBalancingScheme": "INTERNAL_MANAGED",
                "connectionDraining": {
                    "drainingTimeoutSec": 300
                },
                "logConfig": {
                    "enable": false,
                    "optionalMode": "EXCLUDE_ALL_OPTIONAL"
                },
                "localityLbPolicy": "ROUND_ROBIN"
            },
            "fingerprint": "xxxxxxxxxxx",
            "region": "https://www.googleapis.com/compute/v1/projects/<project-id>/regions/us-east1"
        },
        "region": "https://www.googleapis.com/compute/v1/projects/<project-id>/regions/us-east1",
        "fingerprint": "xxxxxxxxxxx"
    },
    "selfLink": "https://www.googleapis.com/compute/v1/projects/<project-id>/regions/us-central1/forwardingRules/host-proj2-tcp-internal-lb1-frontend",
    "loadBalancingScheme": "INTERNAL",
    "subnetwork": "https://www.googleapis.com/compute/v1/projects/<project-id>/regions/us-central1/subnetworks/subnet-1",
    "network": "https://www.googleapis.com/compute/v1/projects/<project-id>/global/networks/central-vpc-hub",
    # Backend Service: https://cloud.google.com/compute/docs/reference/rest/v1/backendServices/get
    "backendService": {
        "kind": "compute#backendService",
        "id": "<backend-service-id>",
        "creationTimestamp": "2021-07-15T18:35:31.122-07:00",
        "name": "host-proj2-tcp-internal-lb1",
        "description": "",
        "selfLink": "https://www.googleapis.com/compute/v1/projects/<project-id>/regions/us-central1/backendServices/host-proj2-tcp-internal-lb1",
        "backends": [
            {
                # Instance Groups: https://cloud.google.com/compute/docs/reference/rest/v1/instanceGroups/get
                "group": {
                    "kind": "compute#instanceGroup",
                    "id": "<group_id>",
                    "creationTimestamp": "2021-07-15T18:31:27.956-07:00",
                    "name": "host-proj2-ig",
                    "description": "This instance group is controlled by Instance Group Manager 'host-proj2-ig'. To modify instances in this group, use the Instance Group Manager API: https://cloud.google.com/compute/docs/reference/latest/instanceGroupManagers",
                    "network": "https://www.googleapis.com/compute/v1/projects/<project-id>/global/networks/central-vpc-hub",
                    "fingerprint": "xxxxxxxxxxx",
                    "zone": "https://www.googleapis.com/compute/v1/projects/<project-id>/zones/us-central1-a",
                    "selfLink": "https://www.googleapis.com/compute/v1/projects/<project-id>/zones/us-central1-a/instanceGroups/host-proj2-ig",
                    "size": 1,
                    "subnetwork": "https://www.googleapis.com/compute/v1/projects/<project-id>/regions/us-central1/subnetworks/subnet-1"
                },
                "balancingMode": "CONNECTION",
                "failover": true
            }
        ],
        "healthChecks": [
            "https://www.googleapis.com/compute/v1/projects/<project-id>/global/healthChecks/tcp-health-check"
        ],
        "timeoutSec": 30,
        "protocol": "TCP",
        "fingerprint": "xxxxxxxx",
        "sessionAffinity": "CLIENT_IP_PORT_PROTO",
        "region": "https://www.googleapis.com/compute/v1/projects/<project-id>/regions/us-central1",
        "failoverPolicy": {
            "disableConnectionDrainOnFailover": false,
            "dropTrafficIfUnhealthy": false,
            "failoverRatio": 0
        },
        "loadBalancingScheme": "INTERNAL",
        "connectionDraining": {
            "drainingTimeoutSec": 300
        },
        "network": "https://www.googleapis.com/compute/v1/projects/<project-id>/global/networks/central-vpc-hub"
    },
    "serviceLabel": "lb",
    "serviceName": "lb.host-proj2-tcp-internal-lb1-frontend.il4.us-central1.lb.<project-id>.internal",
    "networkTier": "PREMIUM",
    "labelFingerprint": "xxxxxxxxxxx",
    "fingerprint": "xxxxxxxxxxx",
    "allPorts": true
}
```


</details>
<br />
