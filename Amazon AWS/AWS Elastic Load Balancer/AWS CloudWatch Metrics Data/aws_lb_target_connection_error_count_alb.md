# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Detecting Backend Connectivity Issues](#example-1) 
    - [Use Case 2 -- Proactive Monitoring for Service Interruptions](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>TargetConnectionErrorCount</b> metric for an AWS Application Load Balancer (ALB) tracks the number of failed attempts to establish connections between the load balancer and the backend target. These connection errors can indicate issues such as network problems, misconfigured security groups, or problems with the backend server’s availability.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: TargetConnectionErrorCount   
* <b>Namespace</b>: AWS/ApplicationELB
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: Target Connection Error Count


# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points, useful for historical analysis or monitoring recent trends. Default time range is last 24 hours.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: Tracks the average number of connection errors, helping to identify periods of frequent backend connectivity problems.
  * <b>Sum</b>: Shows the total number of connection errors, providing insight into the overall connectivity health of backend targets.
  * <b>Minimum</b>: Identifies the lowest number of connection errors, indicating periods when backend connectivity was stable.
  * <b>Maximum</b>: Highlights peak counts of connection errors, which may signal brief outages or configuration issues in the backend.
* <b>Period</b>: Default value is 300 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for near real-time monitoring.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Detecting Backend Connectivity Issues <a name="example-1"></a>
Monitor Target Connection Error Count to identify when the ALB is unable to establish connections with backend targets, which could be caused by network misconfigurations, security group restrictions, or target unavailability.


## Use Case 2: Proactive Monitoring for Service Interruptions <a name="example-2"></a>
Tracking Target Connection Error Count regularly allows for the early detection of backend connectivity issues, preventing service interruptions and reducing downtime.






# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html