# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Identify Unhealthy Targets](#example-1) 
    - [Use Case 2 -- Prevent Service Disruptions](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>UnHealthyHostCount</b> is a metric that tracks the number of unhealthy targets in a Network Load Balancer (NLB) target group. This metric helps identify and troubleshoot issues with target instances that are not responding to health checks or are experiencing performance problems.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: UnHealthyHostCount
* <b>Namespace</b>: AWS/NetworkELB
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: UnHealthy Host Count

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points. This is useful for historical analysis or monitoring recent trends. Default time range is last 24 hours.
* <b>Statistics</b>: Default value is Maximum.
  * <b>Average</b>: The average number of unhealthy targets in a Network Load Balancer (NLB) target group.
  * <b>Sum</b>: The sum of the number of unhealthy targets in a Network Load Balancer (NLB) target group.
  * <b>Minimum</b>: Minimum of the number of unhealthy targets in a Network Load Balancer (NLB) target group.
  * <b>Maximum</b>: Maximum of the number of unhealthy targets in a Network Load Balancer (NLB) target group.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Identify Unhealthy Targets <a name="example-1"></a>
By monitoring this metric, you can quickly identify target instances that are experiencing issues and take corrective actions, such as restarting instances or scaling up the target group.

## Use Case 2: Prevent Service Disruptions <a name="example-2"></a>
By proactively addressing unhealthy targets, you can help prevent service disruptions and maintain high availability.

# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/elasticloadbalancing/latest/network/load-balancer-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html