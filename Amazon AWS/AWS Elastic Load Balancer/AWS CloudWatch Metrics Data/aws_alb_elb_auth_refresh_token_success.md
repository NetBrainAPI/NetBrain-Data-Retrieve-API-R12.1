# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Monitoring Authentication Load on IdP](#example-1) 
    - [Use Case 2 -- Diagnosing Refresh Token Issues](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>ELBAuthRefreshTokenSuccess</b> metric tracks the number of successful refreshes of user claims by the load balancer using a refresh token from the Identity Provider (IdP). This metric is useful for monitoring the reliability and frequency of successful token refreshes, ensuring that authenticated sessions remain valid without reauthentication.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: ELBAuthRefreshTokenSuccess   
* <b>Namespace</b>: AWS/ApplicationELB
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: ELB Auth Refresh Token Success

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points.
* <b>Statistics</b>: Default value is Sum.
  * <b>Sum</b>: Total number of successful token refreshes over the specified period, showing overall refresh success.
  * <b>Minimum</b>: Lowest number of successful refreshes recorded during the period.
  * <b>Maximum</b>: Highest count of refreshes in a single period, helpful for identifying peak usage.
* <b>Period</b>: Default value is 300 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time tracking of refresh token usage.
    * <b>3600 seconds</b> for long-term trend analysis.

# Use Cases Example <a name="example"></a>
## Use Case 1: Monitoring Authentication Load on IdP <a name="example-1"></a>
Track the volume of successful refreshes to assess the load on the IdP, especially during peak periods, ensuring the IdP handles refresh requests effectively.


## Use Case 2: Diagnosing Refresh Token Issues <a name="example-2"></a>
Low or sudden drops in ELB Auth Refresh Token Success could indicate issues with token expiration or connectivity to the IdP, prompting investigation.




# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html