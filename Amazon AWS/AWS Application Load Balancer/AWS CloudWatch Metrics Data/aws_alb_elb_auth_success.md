# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Monitor Authentication Success Trends](#example-1) 
    - [Use Case 2 -- Troubleshoot Authentication Workflow Performance](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>ELBAuthSuccess</b> represents the number of successful authentication actions completed by the Application Load Balancer (ALB). This metric increments once the ALB finishes the authentication workflow, including the retrieval of user claims from an Identity Provider (IdP).

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: ELBAuthSuccess   
* <b>Namespace</b>: AWS/ApplicationELB
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: ELB Authentication Success

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Defines the data range for analysis, defaulting to the past 24 hours for tracking recent authentication trends.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: Calculates the average number of successful authentications over the specified period, useful for observing general trends.
  * <b>Sum</b>: Totals the count of successful authentications within the specified timeframe.
  * <b>Minimum</b>: Indicates the lowest count of successful authentications recorded, identifying intervals with minimal or no authentication events.
  * <b>Maximum</b>: Shows the peak number of successful authentications recorded in any interval during the specified period, valuable for assessing maximum load.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for near real-time monitoring.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Monitor Authentication Success Trends <a name="example-1"></a>
Track successful authentications over time to verify the stability and reliability of the ALB’s authentication service.


## Use Case 2: Troubleshoot Authentication Workflow Performance <a name="example-2"></a>
Use this metric alongside related authentication metrics to identify and diagnose potential issues within the authentication workflow or IdP integration.




# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html