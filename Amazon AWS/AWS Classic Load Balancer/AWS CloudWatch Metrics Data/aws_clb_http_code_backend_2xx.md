# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Performance Monitoring](#example-1) 
    - [Use Case 2 -- Troubleshooting Application Issues](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>HTTPCode_Backend_2XX</b> metric tracks the number of successful HTTP responses (status codes 200-299) received from the backend instances (hosts) registered with a Classic Load Balancer (CLB). This metric is essential for evaluating the health and performance of backend applications, as it indicates the successful handling of requests by the instances behind the load balancer. Monitoring this metric helps ensure that your application is operating efficiently and providing the expected level of service.


# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: HTTPCode_Backend_2XX
* <b>Namespace</b>: AWS/ELB
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: HTTP Code Backend 2XX

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Define the time range to analyze data points, useful for historical analysis or recent monitoring. Default time range is the last 24 hours.
* <b>Statistics</b>: Default value is Sum
  * <b>Average</b>: Useful for observing trends in successful requests over time.
  * <b>Sum</b>: Shows the total count of 2XX responses within the specified period.
  * <b>Minimum</b>: Indicates the lowest count of successful responses recorded, revealing times with reduced performance.
  * <b>Maximum</b>: Highlights peak counts of successful responses, which may indicate periods of high demand.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring to quickly assess application performance.
    * <b>3600 seconds</b> for broader trend analysis over longer durations

# Use Cases Example <a name="example"></a>
## Use Case 1: Performance Monitoring <a name="example-1"></a>

Track the HTTPCode_Backend_2XX metric to ensure that backend instances are handling requests successfully, providing insights into application performance.




## Use Case 2: Troubleshooting Application Issues <a name="example-2"></a>
Monitor for unexpected drops in 2XX responses to identify potential issues with backend instances, allowing for timely intervention to restore service quality.




# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/elasticloadbalancing/latest/classic/elb-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html