# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Traffic Analysis](#example-1) 
    - [Use Case 2 -- Load Balancer Performance Monitoring](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>ProcessedBytes</b> metric tracks the total number of bytes processed by the load balancer, which includes both incoming and outgoing traffic over IPv4 and IPv6. This count reflects the total HTTP header and payload data, including traffic to and from clients, Lambda functions, and, when user authentication is enabled, traffic from an Identity Provider (IdP). Monitoring this metric helps gauge the load balancer's data processing capacity and can assist in identifying traffic trends or potential bottlenecks.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: ProcessedBytes   
* <b>Namespace</b>: AWS/ApplicationELB
* <b>Unit</b>: Bytes
* <b>Display Name in NetBrain</b>: Processed Bytes


# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points. This is useful for historical analysis or monitoring recent trends. The default time range is the last 24 hours.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: The average number of bytes processed during the specified time period.
  * <b>Sum</b>: The total number of bytes processed during the specified time period.
  * <b>Minimum</b>: The least number of bytes processed during the selected period.
  * <b>Maximum</b>: The maximum number of bytes processed during the selected period.
* <b>Period</b>: Default value is 300 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for near real-time monitoring.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Traffic Analysis <a name="example-1"></a>
Monitor the Processed Bytes metric to analyze the volume of data processed by the load balancer over time. This is useful for identifying periods of high traffic and understanding the load on your infrastructure.


## Use Case 2: Load Balancer Performance Monitoring <a name="example-2"></a>
Track changes in processed bytes to identify potential performance issues, such as unexpected spikes in traffic that could lead to latency or resource exhaustion.




# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html