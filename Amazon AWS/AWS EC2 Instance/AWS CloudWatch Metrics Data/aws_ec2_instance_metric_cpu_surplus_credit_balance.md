# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Cost Optimization](#example-1) 
    - [Use Case 2 -- Performance Monitoring](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>CPUSurplusCreditBalance</b> is a metric that measures the number of surplus CPU credits that have been spent by an unlimited burstable performance EC2 instance (like T2, T3, or T4 instances) when its CPUCreditBalance value is zero. These instances have a baseline level of CPU performance and can burst to higher performance levels for short periods of time using CPU credits.


# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: CPUSurplusCreditBalance
* <b>Namespace</b>: AWS/EC2
* <b>Unit</b>: Credits (vCPU-minutes)
* <b>Display Name in NetBrain</b>: CPU Surplus Credit Balance

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points. This is useful for historical analysis or monitoring recent trends. Default time range is last 24 hours.
* <b>Statistics</b>: Default value is Average.
  * <b>Average</b>: The average number of surplus CPU credits consumed over an unlimited burstable performance time period.
  * <b>Sum</b>: The total number of surplus CPU credits consumed over an unlimited burstable performance time period.
  * <b>Minimum</b>: The minimum number of surplus CPU credits consumed at any point over an unlimited burstable performance time period.
  * <b>Maximum</b>: The maximum number of surplus CPU credits consumed at any point over an unlimited burstable performance time period.
* <b>Period</b>: Default value is 300 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Cost Optimization <a name="example-1"></a>
Analyze CPU credit balance to identify identify instances that are consistently using surplus credits


## Use Case 2: Performance Monitoring <a name="example-2"></a>
Track CPU credit balance to indicate that an instance is frequently exceeding its baseline performance and might be experiencing performance degradation.


# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/viewing_metrics_with_cloudwatch.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html