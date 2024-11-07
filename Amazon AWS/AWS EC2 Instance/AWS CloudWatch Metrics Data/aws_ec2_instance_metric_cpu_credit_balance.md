# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Cost Optimization](#example-1) 
    - [Use Case 2 -- Performance Monitoring](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>CPUCreditBalance</b> is a metric that measures the number of CPU credits available for a burstable performance EC2 instance. These instances, for T2, T3, and T4 instances can have a baseline level of CPU performance and can burst to higher performance levels for short periods of time using the CPU credits

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: CPUCreditBalance
* <b>Namespace</b>: AWS/EC2
* <b>Unit</b>: Credits (vCPU-minutes)
* <b>Display Name in NetBrain</b>: CPU Credit Balance

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points. This is useful for historical analysis or monitoring recent trends. Default time range is last 24 hours.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: The average number of CPU credits available for a burstable specified time period.
  * <b>Sum</b>: The total number of CPU credits remaining for a burstable specified time period.
  * <b>Minimum</b>: The minimum number of CPU credits remaining at any point during for a burstable time period.
  * <b>Maximum</b>: The maximum number of CPU credits remaining at any point for a burstable time period.
* <b>Period</b>: Default value is 300 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Cost Optimization <a name="example-1"></a>
Analyze CPU credit balance to identify instances that consistently have a high balance of CPU credits. This could indicate that the instance is overprovisioned and can be downsized to a smaller, more cost-effective instance type.


## Use Case 2: Performance Monitoring <a name="example-2"></a>
Indicate that the instance is frequently running out of CPU credits, leading to performance degradation. By monitoring this metric, we can identify and address these performance bottlenecks.




# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/viewing_metrics_with_cloudwatch.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html