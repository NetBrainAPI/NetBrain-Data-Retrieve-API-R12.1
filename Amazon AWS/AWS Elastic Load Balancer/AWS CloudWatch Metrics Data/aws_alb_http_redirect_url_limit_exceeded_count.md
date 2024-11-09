# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- URL Size Management](#example-1) 
    - [Use Case 2 -- Optimizing Redirect URL Design](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>HTTP_Redirect_Url_Limit_Exceeded_Count</b> metric tracks the number of redirect actions that couldn't be completed because the URL in the response location header exceeded the allowed limit of 8KB. 

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: HTTP_Redirect_Url_Limit_Exceeded_Count   
* <b>Namespace</b>: AWS/ApplicationELB
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: HTTP Redirect URL Limit Exceeded Count

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points. This is useful for historical analysis or monitoring recent trends. The default time range is the last 24 hours.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: The average number of times this limit was exceeded during the time period.
  * <b>Sum</b>: Total number of times the URL size exceeded the limit and the redirect action was not completed.
  * <b>Minimum</b>: The period with the least number of exceeded limits.
  * <b>Maximum</b>: The period with the highest number of exceeded limits.
* <b>Period</b>: Default value is 300 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for near real-time monitoring.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: URL Size Management <a name="example-1"></a>
Track when URL redirection fails due to size limitations, ensuring that URLs are optimized and do not exceed the allowed limit for redirects.




## Use Case 2: Optimizing Redirect URL Design <a name="example-2"></a>
Identify patterns where URLs are consistently too large and make design improvements to avoid triggering the size limit, ensuring seamless user experience during redirects.



# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html