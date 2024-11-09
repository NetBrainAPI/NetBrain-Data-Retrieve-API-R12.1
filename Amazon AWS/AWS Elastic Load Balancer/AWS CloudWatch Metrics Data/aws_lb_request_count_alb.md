# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Performance Optimization](#example-1) 
    - [Use Case 2 -- Identifying Traffic Spikes](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>RequestCount</b> metric tracks the total number of requests processed by the load balancer over both IPv4 and IPv6. This metric only counts requests that the load balancer successfully routed to a target. It does not include requests that were rejected before a target was chosen.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: RequestCount   
* <b>Namespace</b>: AWS/ApplicationELB
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: Request Count


# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points. This is useful for historical analysis or monitoring recent trends. The default time range is the last 24 hours.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: Gives the average number of requests over the selected period, useful for observing trends.
  * <b>Sum</b>: Provides the total number of requests within the specified time period, useful for assessing overall load.
  * <b>Minimum</b>: Shows the period with the least number of requests, indicating times of low traffic.
  * <b>Maximum</b>: Displays the peak number of requests, useful for identifying traffic spikes.
* <b>Period</b>: Default value is 300 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for near real-time monitoring.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Performance Optimization <a name="example-1"></a>
Monitor the Request Count to identify periods of high traffic. This data can be used to optimize load balancing performance or adjust configurations to ensure efficient handling of requests.
## Use Case 2: Identifying Traffic Spikes <a name="example-2"></a>
Analyze this metric to identify unexpected spikes in request counts, which could signal high demand, potential DDoS attacks, or other anomalies in network traffic.




# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html