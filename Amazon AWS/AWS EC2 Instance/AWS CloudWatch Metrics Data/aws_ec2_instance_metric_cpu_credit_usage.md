# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Cost Optimization](#example-1) 
    - [Use Case 2 -- Performance Monitoring](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>CPUCreditUsage</b> metric tracks the number of CPU credits consumed by burstable performance EC2 instances, such as T2 and T3 instance types. These instances are designed to provide a baseline level of CPU performance while allowing for bursts of higher CPU usage through the utilization of CPU credits.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: CPUCreditUsage
* <b>Namespace</b>: AWS/EC2
* <b>Unit</b>: Credits (vCPU-minutes)
* <b>Display Name in NetBrain</b>: CPU Credit Usage

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points. This is useful for historical analysis or monitoring recent trends. Default time range is last 24 hours.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: The average number of CPU credits consumed over a specified time period.
  * <b>Sum</b>: The total number of CPU credits consumed during the specified time period.
  * <b>Minimum</b>: The minimum number of CPU credits consumed at any point during the specified time period.
  * <b>Maximum</b>: The maximum number of CPU credits consumed at any point during the specified time period.
* <b>Period</b>: Default value is 300 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Cost Optimization <a name="example-1"></a>
Analyze CPU credit usage to identify opportunities for resizing instances and reducing costs.


## Use Case 2: Performance Monitoring <a name="example-2"></a>
Track CPU credit consumption to ensure instances meet application performance needs.




# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/viewing_metrics_with_cloudwatch.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html