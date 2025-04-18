# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Identifying Load Balancer Issues](#example-1) 
    - [Use Case 2 -- Enhancing Application Reliability](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>HTTPCode_ELB_5XX</b> metric tracks the number of 5XX HTTP responses generated by the Classic Load Balancer (CLB) itself. These responses indicate server-side errors that occur within the load balancer when it fails to successfully process a valid request. Monitoring this metric is critical for diagnosing load balancer issues that may affect application availability and reliability.


# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: HTTPCode_ELB_5XX
* <b>Namespace</b>: AWS/ELB
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: HTTPCode ELB 5XX

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Define the time range to analyze data points, useful for historical analysis or recent monitoring. Default time range is the last 24 hours.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: Useful for observing general trends in server-side error rates over time.
  * <b>Sum</b>: Shows the total count of 5XX responses generated by the load balancer within the specified period.
  * <b>Minimum</b>: Indicates the lowest number of 5XX responses, revealing times with minimal server errors.
  * <b>Maximum</b>: Highlights peak counts of 5XX responses, which may indicate severe issues with the load balancer's operation.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring to detect sudden increases in server errors.
    * <b>3600 seconds</b> for broader analysis of error trends over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Identifying Load Balancer Issues <a name="example-1"></a>

Monitor 5XX responses to detect and diagnose errors within the load balancer that affect application performance and availability.



## Use Case 2: Enhancing Application Reliability <a name="example-2"></a>
Track spikes in 5XX responses to take proactive measures in resolving load balancer issues, ensuring a smoother user experience and higher application uptime.


# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/elasticloadbalancing/latest/classic/elb-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html