# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Network Traffic Monitoring](#example-1) 
    - [Use Case 2 -- Troubleshooting Connectivity Issues](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>PacketsInFromDestination</b> metric tracks the total number of packets received from the destination through an AWS NAT Gateway. This metric is vital for understanding the volume of inbound packet traffic, which aids in monitoring network performance, diagnosing potential issues, and optimizing resource usage.



# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: PacketsInFromDestination
* <b>Namespace</b>: AWS/NATGateway
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: Packets In From Destination

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Define the time range to analyze data points, useful for historical analysis or recent monitoring. Default time range is the last 24 hours.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: Useful for observing trends in inbound packet traffic over time.
  * <b>Sum</b>: Shows the total number of packets received from the destination within the specified period.
  * <b>Minimum</b>: Indicates the lowest count of packets received, helpful for understanding periods of low activity.
  * <b>Maximum</b>: Highlights peak counts of packets received, which may suggest times of high traffic.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring to quickly assess incoming packet levels.
    * <b>3600 seconds</b> for analyzing overall trends and resource needs over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Network Traffic Monitoring <a name="example-1"></a>
Monitor the PacketsInFromDestination metric to evaluate the volume of inbound packets and ensure that network resources are adequately allocated, helping to maintain optimal performance.

## Use Case 2: Troubleshooting Connectivity Issues <a name="example-2"></a>
Track incoming packet counts to identify potential connectivity problems. A sudden drop in packets may indicate network issues that require immediate attention.


# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/vpc/latest/userguide/metrics-dimensions-nat-gateway.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html