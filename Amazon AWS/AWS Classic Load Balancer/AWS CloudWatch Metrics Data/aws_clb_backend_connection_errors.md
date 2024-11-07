# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Monitoring Backend Health](#example-1) 
    - [Use Case 2 -- Diagnosing Latency Issues](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>BackendConnectionErrors</b> metric tracks the number of connection errors between the Classic Load Balancer (CLB) and the backend instances. Monitoring this metric is crucial for identifying backend connectivity issues that can affect application performance and availability.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: BackendConnectionErrors
* <b>Namespace</b>: AWS/ELB
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: Backend Connection Errors

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Define the time range to analyze data points, useful for historical analysis or recent monitoring. Default time range is the last 24 hours.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: Provides insight into the typical connection error rate over time.
  * <b>Sum</b>: Shows the total count of backend connection errors during the specified timeframe, indicating cumulative issues.
  * <b>Minimum</b>: Indicates the lowest count of connection errors within the timeframe, useful for identifying any periods with minimal issues.
  * <b>Maximum</b>: Highlights peak error occurrences, helping to pinpoint times of degraded backend connectivity.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time error monitoring.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Monitoring Backend Health <a name="example-1"></a>

Track backend connection errors to ensure backend instances are healthy and available, helping to avoid potential connectivity disruptions.

## Use Case 2: Diagnosing Latency Issues <a name="example-2"></a>
Monitor spikes in connection errors to troubleshoot application latency and performance issues, particularly during high traffic periods.



# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/elasticloadbalancing/latest/classic/elb-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html