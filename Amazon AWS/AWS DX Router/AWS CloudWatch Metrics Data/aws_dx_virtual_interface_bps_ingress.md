# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Identifying Traffic Patterns](#example-1) 
    - [Use Case 2 -- Troubleshooting Network Performance](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>VirtualInterfaceBpsIngress</b> metric for AWS Direct Connect (DX) tracks the inbound (ingress) data transfer rate through a virtual interface in bits per second (bps). Monitoring this metric helps you assess the performance of incoming traffic over your Direct Connect Virtual Interface, ensuring that your network can handle the expected data flow.


# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: VirtualInterfaceBpsIngress
* <b>Namespace</b>: AWS/DX
* <b>Unit</b>: Bits per Second (bps)
* <b>Display Name in NetBrain</b>: Virtual Interface Bps Ingress

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points, useful for historical analysis or monitoring recent trends. Default time range is last 24 hours.
* <b>Statistics</b>: Default value is Average.
  * <b>Average</b>: Displays the average ingress throughput over the selected period.
  * <b>Sum</b>: Provides the total ingress throughput during the selected time.
  * <b>Minimum</b>: Identifies periods of minimal ingress bandwidth usage.
  * <b>Maximum</b>: Captures peak ingress bandwidth usage, potentially indicating traffic spikes.
* <b>Period</b>: Default value is 300 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Identifying Traffic Patterns <a name="example-1"></a>
Use this metric to detect unusual patterns in incoming traffic, such as spikes that could indicate unexpected usage or data floods that may need attention.


## Use Case 2: Troubleshooting Network Performance <a name="example-2"></a>
Track ingress throughput to help identify periods of high traffic, which might suggest network congestion or performance bottlenecks that could be optimized.




# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/directconnect/latest/UserGuide/monitoring-cloudwatch.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html