# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Authentication Issue Detection](#example-1) 
    - [Use Case 2 -- Analysis of Load Balancer Reliability](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>ELBAuthError</b> metric tracks the number of user authentication attempts that were unsuccessful due to misconfigurations in the authenticate action, connection issues with the Identity Provider (IdP), or internal errors that prevented the load balancer from completing the authentication flow. Monitoring this metric can help identify and resolve authentication issues to ensure secure access for users.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: ELBAuthError  
* <b>Namespace</b>: AWS/ApplicationELB
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: ELB Auth Error

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: The average number of authentication errors over the specified time period.
  * <b>Sum</b>: The total number of authentication errors over the specified time period.
  * <b>Minimum</b>: The lowest count of errors during the selected period, indicating times with fewer issues.
  * <b>Maximum</b>: The highest count of errors during the selected period, useful for spotting spikes.
* <b>Period</b>: Default value is 300 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Authentication Issue Detection <a name="example-1"></a>
Use ELB Auth Error to detect and address misconfigurations or connection problems with the IdP. A higher error count indicates potential issues in the authentication setup that need immediate attention.



## Use Case 2: Analysis of Load Balancer Reliability <a name="example-2"></a>
Track ELB Auth Error to evaluate the reliability of the load balancer in handling authentication processes. Persistent errors might indicate a need for system adjustments or improvements in the authentication configuration.





# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html