# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Detecting Network Congestion](#example-1) 
    - [Use Case 2 -- Cost Optimization](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>VirtualInterfaceBpsEgress</b> metric for AWS Direct Connect (DX) tracks the outbound (egress) data transfer rate through a virtual interface in bits per second (bps). This metric is essential for monitoring the bandwidth usage of your Direct Connect link, helping ensure that your data transfer meets the performance requirements of your network.



# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: VirtualInterfaceBpsEgress
* <b>Namespace</b>: AWS/DX
* <b>Unit</b>: Bits per Second (bps)
* <b>Display Name in NetBrain</b>: Virtual Interface Bps Egress

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points, useful for historical analysis or monitoring recent trends. Default time range is last 24 hours.
* <b>Statistics</b>: Default value is Average.
  * <b>Average</b>: Shows the average egress throughput over the selected period.
  * <b>Sum</b>: Provides the total egress throughput over the specified time.
  * <b>Minimum</b>: Identifies periods of minimal egress bandwidth usage.
  * <b>Maximum</b>: Captures peak bandwidth usage, potentially indicating high traffic periods.
* <b>Period</b>: Default value is 300 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Detecting Network Congestion <a name="example-1"></a>
Analyze egress bandwidth to identify periods of high usage, which may indicate network congestion or bandwidth limitations that require optimization.



## Use Case 2: Cost Optimization <a name="example-2"></a>
Monitor bandwidth usage to identify times of excessive data transfer, allowing for the adjustment of workloads to optimize costs related to data transfer.




# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/directconnect/latest/UserGuide/monitoring-cloudwatch.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html