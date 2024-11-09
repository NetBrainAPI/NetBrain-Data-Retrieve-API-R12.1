# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Access Denial Monitoring](#example-1) 
    - [Use Case 2 -- Troubleshooting User Access Issues](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>ELBAuthFailure</b> metric counts the number of user authentication attempts that failed because the Identity Provider (IdP) denied access or an authorization code was reused. This metric is useful for monitoring authorization issues and ensuring users meet access requirements.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: ELBAuthFailure   
* <b>Namespace</b>: AWS/ApplicationELB
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: ELB Auth Failure

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: The average number of failed authentications over the specified time period.
  * <b>Sum</b>: The total number of failed authentications over the specified time period.
  * <b>Minimum</b>: The lowest count of failures during the selected period, indicating periods with minimal issues.
  * <b>Maximum</b>: The highest count of failures during the selected period, useful for spotting peaks in denial incidents.
* <b>Period</b>: Default value is 300 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for close to real-time monitoring.
    * <b>3600 seconds</b> for broader trend analysis of access failures.

# Use Cases Example <a name="example"></a>
## Use Case 1: Access Denial Monitoring <a name="example-1"></a>
Track ELB Auth Failure to identify times when users were denied access by the IdP. Sudden increases may indicate stricter policies or issues with user permissions.




## Use Case 2: Troubleshooting User Access Issues <a name="example-2"></a>
Investigate ELB Auth Failure peaks to determine root causes of denied access, whether from IdP policy changes, user role adjustments, or authorization issues.






# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html