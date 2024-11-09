# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Load Balancer Performance Tuning](#example-1) 
    - [Use Case 2 -- Capacity Planning and Scaling](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>ActiveConnectionCount</b> metric measures the total number of concurrent TCP connections that are active between clients and the load balancer, as well as between the load balancer and the targets. This metric provides an indication of the load balancer's traffic volume and helps in managing its capacity and performance.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: ActiveConnectionCount
* <b>Namespace</b>: AWS/ApplicationELB
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: Active Connection Count

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points, useful for historical analysis or monitoring recent trends. Default time range is last 24 hours.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: Provides the average number of active connections over a selected period, useful for observing general connection trends.
  * <b>Sum</b>: Displays the total number of active connections within the specified time range, useful for understanding the overall connection load.
  * <b>Minimum</b>: Indicates periods with least active connections, showing times of low or no traffic.
  * <b>Maximum</b>: Shows the peak number of active connections, helping to identify load peaks.
* <b>Period</b>: Default value is 300 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Load Balancer Performance Tuning <a name="example-1"></a>
Use this metric to identify periods with high active connections and ensure the ALB is performing optimally, especially during peak traffic times or when scaling is required.


## Use Case 2: Capacity Planning and Scaling <a name="example-2"></a>
Analyze the Active Connection Count metric over time to help plan for scaling decisions, ensuring the load balancer has sufficient capacity to handle increasing traffic volumes.



# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html