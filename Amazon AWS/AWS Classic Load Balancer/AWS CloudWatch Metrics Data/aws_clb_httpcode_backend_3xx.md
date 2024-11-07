# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Redirection Analysis](#example-1) 
    - [Use Case 2 -- Troubleshooting Unexpected Redirects](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>HTTPCode_Backend_3XX</b> metric tracks the number of 3XX HTTP responses from backend instances behind a Classic Load Balancer (CLB). Monitoring this metric is crucial for understanding redirection patterns, which impact user experience and network efficiency.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: HTTPCode_Backend_3XX
* <b>Namespace</b>: AWS/ELB
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: HTTPCode Backend 3XX

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Define the time range to analyze data points, useful for historical analysis or recent monitoring. Default time range is the last 24 hours.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: Useful for observing general redirection trends over time.
  * <b>Sum</b>: Shows the total count of 3XX responses from backend instances within the specified period.
  * <b>Minimum</b>: Indicates the lowest number of 3XX responses, revealing times with minimal redirections.
  * <b>Maximum</b>: Highlights peak redirection counts, which can indicate unusual traffic behavior.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring to detect high redirection rates quickly.
    * <b>3600 seconds</b> for broader analysis of redirection trends over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Redirection Analysis <a name="example-1"></a>

Monitor 3XX responses to understand redirection patterns, especially when backend resources are moved or load balancing directs users to alternate resources.

## Use Case 2: Troubleshooting Unexpected Redirects <a name="example-2"></a>
Track spikes in 3XX responses to identify potential misconfigurations or unexpected traffic redirection, allowing for timely adjustments to backend settings or URL paths.

# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/elasticloadbalancing/latest/classic/elb-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html