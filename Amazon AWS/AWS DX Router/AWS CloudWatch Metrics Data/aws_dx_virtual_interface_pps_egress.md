# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Identifying Network Congestion](#example-1) 
    - [Use Case 2 -- Optimizing Data Flow](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>VirtualInterfacePpsEgress</b> metric for AWS Direct Connect (DX) tracks the outbound (egress) packet rate through a virtual interface in packets per second (pps). This metric is crucial for monitoring the rate at which packets are leaving the Direct Connect Virtual Interface, helping to ensure that traffic is being transmitted at the expected rates and identifying potential congestion or packet loss issues.


# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: VirtualInterfacePpsEgress
* <b>Namespace</b>: AWS/DX
* <b>Unit</b>: Packets per Second (pps)
* <b>Display Name in NetBrain</b>: Virtual Interface Pps Egress

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points, useful for historical analysis or monitoring recent trends. Default time range is last 24 hours.
* <b>Statistics</b>: Default value is Average.
  * <b>Average</b>: Shows the average packet rate egress over the selected period.
  * <b>Sum</b>: Provides the total number of packets transmitted during the selected time.
  * <b>Minimum</b>: Identifies periods of minimal egress packet transmission.
  * <b>Maximum</b>: Captures peak packet rates, potentially indicating moments of high outbound traffic.
* <b>Period</b>: Default value is 300 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Identifying Network Congestion <a name="example-1"></a>
Use this metric to detect periods of high packet transmission that could indicate network congestion or insufficient capacity, helping to optimize the link.


## Use Case 2: Optimizing Data Flow <a name="example-2"></a>
By tracking the number of packets being sent out through the Direct Connect link, you can identify if any changes need to be made to manage bandwidth and improve overall network performance.


# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/directconnect/latest/UserGuide/monitoring-cloudwatch.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html