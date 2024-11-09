# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Monitoring URL Forwarding](#example-1) 
    - [Use Case 2 -- Handling Maintenance Redirects](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>HTTP_Redirect_Count</b> metric tracks the number of successful HTTP redirect actions processed by the Application Load Balancer (ALB). Redirect actions are used to send HTTP requests to a different URL, allowing the ALB to handle URL forwarding for clients based on specific rules or conditions.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: HTTP_Redirect_Count   
* <b>Namespace</b>: AWS/ApplicationELB
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: HTTP Redirect Count

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points. This is useful for historical analysis or monitoring recent trends. The default time range is the last 24 hours.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: The average number of redirect actions per time unit.
  * <b>Sum</b>: Total number of successful redirect actions in the specified time period.
  * <b>Minimum</b>: The period with the least number of successful redirect actions.
  * <b>Maximum</b>: The period with the highest number of successful redirect actions.
* <b>Period</b>: Default value is 300 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for near real-time monitoring.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Monitoring URL Forwarding <a name="example-1"></a>
Track the number of successful HTTP redirects to ensure that requests are being properly forwarded to new URLs as per business or routing requirements.



## Use Case 2: Handling Maintenance Redirects <a name="example-2"></a>
Monitor redirect counts for maintenance page configurations, ensuring that users are redirected to an appropriate page during downtime or scheduled maintenance.



# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html