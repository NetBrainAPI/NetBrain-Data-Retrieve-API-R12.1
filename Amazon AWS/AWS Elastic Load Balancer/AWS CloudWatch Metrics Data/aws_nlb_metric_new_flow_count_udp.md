# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Identify Traffic Spikes](#example-1) 
    - [Use Case 2 -- Identify Unusual Traffic Patterns](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>NewFlowCount_UDP</b> is a metric that tracks the number of new UDP flow connections established by a Network Load Balancer (NLB) within a specific period. By monitoring this metric, you can identify network performance issues, security threats, and optimize NLB configuration.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: NewFlowCount_UDP
* <b>Namespace</b>: AWS/NetworkELB
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: New Flow Count UDP

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points. This is useful for historical analysis or monitoring recent trends. Default time range is last 24 hours.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: The average number of new UDP flow connections established by a Network Load Balancer (NLB) within a specific period.
  * <b>Sum</b>: The sum of the number of new UDP flow connections established by a Network Load Balancer (NLB) within a specific period.
  * <b>Minimum</b>: Minimum of the number of new UDP flow connections established by a Network Load Balancer (NLB) within a specific period.
  * <b>Maximum</b>: Maximum of the number of new UDP flow connections established by a Network Load Balancer (NLB) within a specific period.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Identify Traffic Spikes <a name="example-1"></a>
By monitoring NewFlowCount, you can identify sudden increases in UDP traffic to your application. This can help you proactively scale your infrastructure to handle increased load.

## Use Case 2: Identify Unusual Traffic Patterns <a name="example-2"></a>
Analyzing the distribution of NewFlowCount_UDP can help you identify unusual traffic patterns that may require further investigation.

# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/elasticloadbalancing/latest/network/load-balancer-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html