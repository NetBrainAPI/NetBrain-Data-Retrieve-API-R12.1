# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Capacity Planning](#example-1) 
    - [Use Case 2 -- Diagnosing Performance Issues](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>Spillover Count</b> metric tracks the number of requests that are not handled by the Classic Load Balancer (CLB) because the load balancer's capacity has been exceeded. This situation typically occurs when the backend instances are overwhelmed and cannot process additional requests. Monitoring the Spillover Count is crucial for understanding traffic demands and ensuring sufficient resources are available to handle incoming requests.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: SpilloverCount
* <b>Namespace</b>: AWS/ELB
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: Spillover Count

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Define the time range to analyze data points, useful for historical analysis or recent monitoring. Default time range is the last 24 hours.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: Useful for observing general trends in spillover requests over time.
  * <b>Sum</b>: Shows the total number of spillover requests that were not processed by the load balancer within the specified period.
  * <b>Minimum</b>: Indicates the lowest number of spillover requests recorded, revealing times with minimal load.
  * <b>Maximum</b>: Highlights peak spillover counts, which may indicate critical capacity issues during high traffic periods.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring to detect sudden increases in spillover requests.
    * <b>3600 seconds</b> for broader trend analysis of latency trends over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Capacity Planning <a name="example-1"></a>
Monitor the Spillover Count to assess whether current backend resources are adequate to handle traffic loads, aiding in scaling decisions.


## Use Case 2: Diagnosing Performance Issues <a name="example-2"></a>
Track spikes in spillover requests to identify potential backend performance issues or misconfigurations that prevent the load balancer from handling incoming traffic effectively.




# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/elasticloadbalancing/latest/classic/elb-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html