# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Identifying Traffic Spikes](#example-1) 
    - [Use Case 2 -- Connection Efficiency Analysis](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>NewConnectionCount</b> metric tracks the total number of new TCP connections established between clients and the load balancer, as well as between the load balancer and its targets. Monitoring this metric is essential for understanding the rate at which new connections are initiated, which can be helpful for identifying patterns in traffic spikes or potential issues with connection management.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: NewConnectionCount   
* <b>Namespace</b>: AWS/ApplicationELB
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: New Connection Count

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points. This is useful for historical analysis or monitoring recent trends. The default time range is the last 24 hours.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: The average number of new connections established during the time period.
  * <b>Sum</b>: The total number of new connections established during the selected period.
  * <b>Minimum</b>: The least number of new connections established during the selected period.
  * <b>Maximum</b>: The maximum number of new connections established during the selected period.
* <b>Period</b>: Default value is 300 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for near real-time monitoring.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Identifying Traffic Spikes <a name="example-1"></a>
Monitor new connection counts to identify sudden spikes in traffic, which could indicate unexpected surges or potential issues.



## Use Case 2: Connection Efficiency Analysis <a name="example-2"></a>
Track this metric to determine the efficiency of the load balancer in establishing new connections. If the count is unusually low, it may indicate issues with traffic distribution or load balancing configuration.




# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html