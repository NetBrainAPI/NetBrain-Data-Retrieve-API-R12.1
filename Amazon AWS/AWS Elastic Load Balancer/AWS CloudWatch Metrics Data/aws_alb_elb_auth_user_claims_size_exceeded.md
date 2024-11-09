# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Monitor Compliance with IdP Data Size Limits](#example-1) 
    - [Use Case 2 -- Diagnose Authentication Workflow Issues](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>ELBAuthUserClaimsSizeExceeded</b> metric indicates the number of times a configured Identity Provider (IdP) returned user claims that exceeded the maximum allowable size of 11K bytes during the authentication process. This metric is useful for identifying instances where user claim data exceeded acceptable limits, which could impact load balancer processing performance.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: ELBAuthUserClaimsSizeExceeded   
* <b>Namespace</b>: AWS/ApplicationELB
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: ELB Auth User Claims Size Exceeded

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points. This helps in analyzing historical trends or monitoring recent occurrences. The default time range is the last 24 hours.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: The average number of oversized user claims within the specified time range, helping to understand typical occurrences.
  * <b>Sum</b>: The total number of oversized user claims, useful for assessing overall volume and impact.
  * <b>Minimum</b>: Periods where there were no oversized claims, indicating times when the IdP returned compliant data sizes.
  * <b>Maximum</b>: The peak number of occurrences within a single period, indicating the highest instance count of oversized user claims.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for near real-time monitoring.
    * <b>3600 seconds</b> for observing broader trends over extended durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Monitor Compliance with IdP Data Size Limits <a name="example-1"></a>
Track this metric to ensure that IdP responses stay within size limits, preventing potential authentication delays or failures in the Application Load Balancer.



## Use Case 2: Diagnose Authentication Workflow Issues <a name="example-2"></a>
By monitoring the occurrences of oversized user claims, you can work with the IdP to troubleshoot data size problems that may interrupt the ALB's authentication flow.





# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html