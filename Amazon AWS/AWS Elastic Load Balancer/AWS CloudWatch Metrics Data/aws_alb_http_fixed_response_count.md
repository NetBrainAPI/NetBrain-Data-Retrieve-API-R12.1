# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Monitoring Static Content Responses](#example-1) 
    - [Use Case 2 -- Custom Response Evaluation](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>HTTP_Fixed_Response_Count</b> metric tracks the number of successful fixed-response actions processed by the Application Load Balancer (ALB). Fixed responses are pre-configured responses that are returned by the ALB without forwarding the request to a target. This can be useful for scenarios like redirecting clients or responding with static content.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: HTTP_Fixed_Response_Count   
* <b>Namespace</b>: AWS/ApplicationELB
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: HTTP Fixed Response Count

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points. This is useful for historical analysis or monitoring recent trends. The default time range is the last 24 hours.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: The average number of fixed responses per time unit.
  * <b>Sum</b>: Total number of fixed-response actions in the specified time period.
  * <b>Minimum</b>: The period with the least number of successful fixed-response actions.
  * <b>Maximum</b>: The period with the highest number of successful fixed-response actions.
* <b>Period</b>: Default value is 300 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for near real-time monitoring.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Monitoring Static Content Responses <a name="example-1"></a>
Track the number of successful fixed responses to ensure that predefined static contents are being returned as expected.


## Use Case 2: Custom Response Evaluation <a name="example-2"></a>
Evaluate the frequency of custom responses (e.g., for maintenance pages or redirects) to understand the use and effectiveness of fixed responses in your ALB configuration.


# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html