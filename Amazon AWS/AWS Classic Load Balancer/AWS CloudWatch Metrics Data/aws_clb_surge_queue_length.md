# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Traffic Management](#example-1) 
    - [Use Case 2 -- Performance Optimization](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>SurgeQueueLength</b> metric tracks the number of requests that are waiting in the surge queue of a Classic Load Balancer (CLB). The surge queue temporarily holds requests when the load balancer cannot forward them to backend instances due to capacity constraints or high traffic volumes. Monitoring this metric is vital for understanding how well the load balancer is managing incoming traffic and for identifying potential bottlenecks in the application’s ability to handle requests.


# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: SurgeQueueLength
* <b>Namespace</b>: AWS/ELB
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: Surge Queue Length

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Define the time range to analyze data points, useful for historical analysis or recent monitoring. Default time range is the last 24 hours.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: Useful for observing trends in surge queue length over time.
  * <b>Sum</b>: Shows the total number of requests that have been queued during the specified period.
  * <b>Minimum</b>: Indicates the lowest surge queue length recorded, revealing times of optimal performance.
  * <b>Maximum</b>: Highlights peak surge queue lengths, which may indicate periods of high traffic and potential capacity issues.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring to quickly assess the current state of request queuing.
    * <b>3600 seconds</b> for broader analysis of trends over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Traffic Management <a name="example-1"></a>
Monitor the  surge queue lengths to identify when requests are being queued due to backend capacity limitations, allowing for proactive scaling of resources.


## Use Case 2: Performance Optimization <a name="example-2"></a>
Track surge queue lengths to determine if additional backend instances are needed during peak traffic times to maintain optimal response times.



# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/elasticloadbalancing/latest/classic/elb-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html