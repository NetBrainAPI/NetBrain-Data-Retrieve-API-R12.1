# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Identify Unhealthy Targets](#example-1) 
    - [Use Case 2 -- Identify Network Issues](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>ActiveZonalShiftHostCount</b> is a metric that tracks the number of active host connections for a Network Load Balancer (NLB) that are being shifted to different Availability Zones due to health checks or other factors. By monitoring this metric, you can identify potential performance or configuration issues with your NLB and target groups.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: ActiveZonalShiftHostCount
* <b>Namespace</b>: AWS/NetworkELB
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: Active Zonal Shift Host Count

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points. This is useful for historical analysis or monitoring recent trends. Default time range is last 24 hours.
* <b>Statistics</b>: Default value is Average.
  * <b>Average</b>: The average number of active host connections for a Network Load Balancer (NLB) that are being shifted to different Availability Zones due to health checks or other factors.
  * <b>Sum</b>: The sum of the number of active host connections for a Network Load Balancer (NLB) that are being shifted to different Availability Zones due to health checks or other factors.
  * <b>Minimum</b>: The minimum of the number of active host connections for a Network Load Balancer (NLB) that are being shifted to different Availability Zones due to health checks or other factors.
  * <b>Maximum</b>: The maximum of the number of active host connections for a Network Load Balancer (NLB) that are being shifted to different Availability Zones due to health checks or other factors.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Identify Unhealthy Targets <a name="example-1"></a>
This metric can help identify target groups with high rates of health check failures, indicating potential performance or configuration issues.

## Use Case 2: Identify Network Issues <a name="example-2"></a>
Sudden spikes in ActiveZonalShiftHostCount can indicate network issues that are affecting the availability of the application.

# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/elasticloadbalancing/latest/network/load-balancer-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html