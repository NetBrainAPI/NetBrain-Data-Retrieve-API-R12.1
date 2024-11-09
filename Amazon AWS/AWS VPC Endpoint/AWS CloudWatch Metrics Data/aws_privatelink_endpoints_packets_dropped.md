# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Troubleshooting Network Issues](#example-1) 
    - [Use Case 2 -- Ensuring Network Reliability](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>PacketsDropped</b> metric for VPC Endpoints tracks the number of network packets that were dropped due to issues such as resource constraints, configuration errors, or network congestion. Monitoring this metric is crucial for ensuring network reliability and troubleshooting packet loss that could affect application performance.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: PacketsDropped
* <b>Namespace</b>: AWS/PrivateLinkEndpoints
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: Packets Dropped

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points, useful for historical analysis or monitoring recent trends. Default time range is last 24 hours.
* <b>Statistics</b>: Default value is Average.
  * <b>Average</b>: Provides a general view of packet drop trends over the selected period.
  * <b>Sum</b>: Displays the total number of dropped packets during the specified timeframe.
  * <b>Minimum</b>: Highlights periods of minimal packet drops.
  * <b>Maximum</b>: Identifies peak packet drop occurrences.
* <b>Period</b>: Default value is 300 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Troubleshooting Network Issues <a name="example-1"></a>
Track Packets Dropped to diagnose network problems, such as congestion or misconfigurations, which may be causing packet loss and affecting application performance.



## Use Case 2: Ensuring Network Reliability <a name="example-2"></a>
Monitor dropped packets over time to ensure that network resources and configurations can reliably handle traffic without significant data loss.



# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/vpc/latest/privatelink/privatelink-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html