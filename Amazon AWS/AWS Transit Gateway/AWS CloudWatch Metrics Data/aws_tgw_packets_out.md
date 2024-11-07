# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Monitoring Inbound Traffic Volume](#example-1) 
    - [Use Case 2 -- Troubleshooting Network Performance](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>PacketsIn</b> metric tracks the total volume of inbound data processed by an AWS Transit Gateway. This metric is useful for monitoring the amount of data entering the network through the Transit Gateway, helping to assess traffic load and manage network performance.



# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: PacketsOut
* <b>Namespace</b>: AWS/TransitGateway
* <b>Unit</b>: Packets
* <b>Display Name in NetBrain</b>: Packets Out

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Define the time range to analyze data points, useful for historical analysis or recent monitoring. Default time range is the last 24 hours.
* <b>Statistics</b>: Default value is Sum
  * <b>Average</b>: Useful for observing general trends in inbound data over time.
  * <b>Sum</b>: Shows the total volume of data received within the specified period.
  * <b>Minimum</b>: Indicates the lowest recorded volume of inbound data, useful for identifying low-traffic periods.
  * <b>Maximum</b>: Highlights peak inbound data volumes, which may indicate times of high network usage.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring to quickly assess inbound traffic volume.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Monitoring Inbound Traffic Volume <a name="example-1"></a>
Track the Packets metric to gauge the volume of inbound data handled by the Transit Gateway, ensuring adequate network capacity to handle traffic load.

## Use Case 2: Troubleshooting Network Performance <a name="example-2"></a>
Use this metric to identify periods of unexpectedly high inbound traffic that may impact performance, enabling timely intervention to optimize network efficiency.


# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/vpc/latest/tgw/transit-gateway-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html