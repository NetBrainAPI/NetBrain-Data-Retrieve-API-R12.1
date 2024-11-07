# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Cost Optimization](#example-1) 
    - [Use Case 2 -- Performance Monitoring](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>CPUSurplusCreditsCharged</b> is a metric that measures the number of surplus CPU credits consumed by an unlimited burstable performance EC2 instance (like T2, T3, or T4 instances) that have not been paid down by earned CPU credits. These instances have a baseline level of CPU performance and can burst to higher performance levels for short periods of time using CPU credits.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: CPUSurplusCreditsCharged
* <b>Namespace</b>: AWS/EC2
* <b>Unit</b>: Credits (vCPU-minutes)
* <b>Display Name in NetBrain</b>: CPU Surplus Credits Charged

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points. This is useful for historical analysis or monitoring recent trends. Default time range is last 24 hours.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: The average number of surplus CPU credits consumed over a specified time period.
  * <b>Sum</b>: The total number of surplus CPU credits consumed during the specified time period.
  * <b>Minimum</b>: The minimum number of surplus CPU credits consumed at any point during the specified time period.
  * <b>Maximum</b>: The maximum number of surplus CPU credits consumed at any point during the specified time period.
* <b>Period</b>: Default value is 300 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Cost Optimization <a name="example-1"></a>
Identify instances that are consistently consuming surplus credits. This indicates that the instance is frequently exceeding its baseline performance and incurring additional costs.

## Use Case 2: Performance Monitoring <a name="example-2"></a>
High credits being charged can signal that an instance is frequently experiencing performance bottlenecks and is unable to meet its workload demands.


# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/viewing_metrics_with_cloudwatch.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html