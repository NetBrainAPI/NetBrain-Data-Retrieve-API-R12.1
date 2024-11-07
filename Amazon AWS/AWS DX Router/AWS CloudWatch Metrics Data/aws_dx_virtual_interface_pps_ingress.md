# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Identifying Network Congestion](#example-1) 
    - [Use Case 2 -- Analyzing Data Flow Patterns](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>VirtualInterfacePpsIngress</b> metric for AWS Direct Connect (DX) tracks the inbound (ingress) packet rate through a virtual interface in packets per second (pps). Monitoring this metric is vital for assessing the rate at which packets are being received on your Direct Connect virtual interface, helping identify issues related to traffic spikes, congestion, or potential bottlenecks in data transfer.



# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: VirtualInterfacePpsIngress
* <b>Namespace</b>: AWS/DX
* <b>Unit</b>: Packets per Second (pps)
* <b>Display Name in NetBrain</b>: Virtual Interface Pps Ingress

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points, useful for historical analysis or monitoring recent trends. Default time range is last 24 hours.
* <b>Statistics</b>: Default value is Sum
  * <b>Average</b>: Displays the average ingress packet rate over the selected period.
  * <b>Sum</b>: Provides the total number of packets received during the selected time.
  * <b>Minimum</b>: Identifies periods of minimal ingress packet reception.
  * <b>Maximum</b>: Captures peak ingress packet rates, potentially indicating high traffic periods.
* <b>Period</b>: Default value is 300 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Identifying Network Congestion <a name="example-1"></a>
Use this metric to detect unusual packet rates that could indicate network congestion or an overload on the Direct Connect link, allowing for proactive adjustments.



## Use Case 2: Analyzing Data Flow Patterns <a name="example-2"></a>
Analyze ingress traffic patterns to identify trends in data flows, helping with capacity planning or detecting unexpected surges in traffic that might need to be addressed.

# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/directconnect/latest/UserGuide/monitoring-cloudwatch.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html