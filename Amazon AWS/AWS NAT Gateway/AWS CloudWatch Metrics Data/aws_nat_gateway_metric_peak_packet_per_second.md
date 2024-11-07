# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Traffic Surge Analysis](#example-1) 
    - [Use Case 2 -- Network Performance Monitoring](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>PeakPacketsPerSecond</b> metric measures the highest number of packets processed per second by an AWS NAT Gateway. This metric is crucial for assessing the peak performance capabilities of the NAT Gateway and understanding traffic spikes that could affect network performance.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: PeakPacketsPerSecond
* <b>Namespace</b>: AWS/NATGateway
* <b>Unit</b>: Count/Second
* <b>Display Name in NetBrain</b>: Peak Packet Per Second

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Define the time range to analyze data points, useful for historical analysis or recent monitoring. Default time range is the last 24 hours.
* <b>Statistics</b>: Default value is Maximum.
  * <b>Average</b>: Useful for observing general packet flow trends over time.
  * <b>Sum</b>: Displays the total number of packets processed over the specified period.
  * <b>Minimum</b>: Indicates the lowest packet rate, helping to identify periods of low activity.
  * <b>Maximum</b>: Represents the highest packet processing rate, indicating peak traffic conditions.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring to detect immediate changes in packet flow.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Traffic Surge Analysis <a name="example-1"></a>
Monitor the PeakPacketsPerSecond metric during high-demand periods to understand how the NAT Gateway handles sudden spikes in traffic, which is vital for capacity planning and resource allocation.

## Use Case 2: Network Performance Monitoring <a name="example-2"></a>
Track this metric to ensure the NAT Gateway operates efficiently under varying load conditions. Identifying peak packet rates helps to optimize configurations and mitigate potential bottlenecks.

# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/vpc/latest/userguide/metrics-dimensions-nat-gateway.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html