# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Cost Optimization](#example-1) 
    - [Use Case 2 -- Diagnosing Unexpected Traffic Spikes](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>ConsumedLCUs</b> metric for an AWS Application Load Balancer (ALB) tracks the total Load Balancer Capacity Units (LCUs) consumed, representing load balancer usage based on resource consumption. Monitoring this metric helps you optimize resource allocation and manage costs by understanding how much load balancer capacity is used over time.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: ConsumedLCUs 
* <b>Namespace</b>: AWS/ApplicationELB
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: Consumed LCUs

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points, useful for historical analysis or monitoring recent trends. Default time range is last 24 hours.
* <b>Statistics</b>: Default value is Average.
  * <b>Average</b>: Provides the average rate of TLS negotiation errors over the selected period.
  * <b>Sum</b>: Shows total LCUs consumed, indicating cumulative resource usage for cost assessment.
  * <b>Minimum</b>: Highlights periods with no errors, which can help identify successful connection times.
  * <b>Maximum</b>: Identifies peak usage periods, which can aid in capacity planning.
* <b>Period</b>: Default value is 300 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Cost Optimization <a name="example-1"></a>
Monitor Consumed LCUs to understand how much capacity your ALB is using, helping to identify cost-saving opportunities by scaling resources according to demand.


## Use Case 2: Diagnosing Unexpected Traffic Spikes <a name="example-2"></a>
By monitoring Consumed LCUs, you can quickly detect unusual spikes in traffic or resource consumption, which may indicate sudden surges due to promotional events or potential bot activity. This helps you proactively respond by adjusting capacity as needed.



# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html