# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Identify Overprovisioned Tasks](#example-1) 
    - [Use Case 2 -- Optimize Resource Allocation](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>ConsumedLCUs</b> is a metric that tracks the number of Linux Container Units (LCUs) consumed by Amazon ECS tasks. LCUs measure the relative CPU and memory capacity of your tasks. By monitoring this metric, you can optimize the resource allocation of your ECS tasks and ensure optimal performance.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: ConsumedLCUs
* <b>Namespace</b>: AWS/NetworkELB
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: Consumed LCUs

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points. This is useful for historical analysis or monitoring recent trends. Default time range is last 24 hours.
* <b>Statistics</b>: Default value is Average.
  * <b>Average</b>: The average number of Linux Container Units (LCUs) consumed by Amazon ECS tasks.
  * <b>Sum</b>: The sum of the number of Linux Container Units (LCUs) consumed by Amazon ECS tasks.
  * <b>Minimum</b>: Minimum of the number of Linux Container Units (LCUs) consumed by Amazon ECS tasks.
  * <b>Maximum</b>: Maximum of the number of Linux Container Units (LCUs) consumed by Amazon ECS tasks.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Identify Overprovisioned Tasks <a name="example-1"></a>
If a task consistently consumes fewer LCUs than its allocated capacity, you can consider downsizing it to a smaller instance type to reduce costs.

## Use Case 2: Optimize Resource Allocation <a name="example-2"></a>
By analyzing the LCU consumption of your tasks, you can identify opportunities to optimize resource allocation and reduce costs.

# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/elasticloadbalancing/latest/network/load-balancer-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html