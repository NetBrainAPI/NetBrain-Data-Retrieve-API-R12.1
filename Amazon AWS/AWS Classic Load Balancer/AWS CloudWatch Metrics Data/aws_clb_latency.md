# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Performance Monitoring](#example-1) 
    - [Use Case 2 -- Diagnosing Performance Issues](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>Latency</b> metric measures the time taken for a request to be processed by the Classic Load Balancer (CLB) and for the response to be sent back to the client. This metric is crucial for assessing the performance of the load balancer and the backend instances it distributes traffic to. Monitoring latency helps identify performance bottlenecks and ensures a smooth user experience.



# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: Latency
* <b>Namespace</b>: AWS/ELB
* <b>Unit</b>: Seconds
* <b>Display Name in NetBrain</b>: Latency

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Define the time range to analyze data points, useful for historical analysis or recent monitoring. Default time range is the last 24 hours.
* <b>Statistics</b>: Default value is Average.
  * <b>Average</b>: Useful for observing general latency trends over time.
  * <b>Sum</b>: Shows the total latency accumulated over the specified period, but is less commonly used for latency.
  * <b>Minimum</b>: Indicates the shortest response time recorded, revealing optimal performance instances.
  * <b>Maximum</b>: Highlights peak response times, which may signal performance issues during high traffic periods.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring to quickly detect latency spikes.
    * <b>3600 seconds</b> for broader trend analysis of latency trends over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Performance Monitoring <a name="example-1"></a>
Track latency to ensure the load balancer and backend instances are responding in a timely manner, enhancing the overall user experience.

## Use Case 2: Diagnosing Performance Issues <a name="example-2"></a>
Monitor latency spikes to identify potential bottlenecks in the application architecture or backend processing, allowing for targeted optimizations.



# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/elasticloadbalancing/latest/classic/elb-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html