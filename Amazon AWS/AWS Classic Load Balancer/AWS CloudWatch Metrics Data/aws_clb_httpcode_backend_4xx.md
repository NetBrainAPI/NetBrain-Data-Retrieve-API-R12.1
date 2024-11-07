# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Monitoring Client-Side Errors](#example-1) 
    - [Use Case 2 -- Troubleshooting Application Accessibility](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>HTTPCode_Backend_4XX</b> metric tracks the number of 4XX HTTP responses from backend instances behind a Classic Load Balancer (CLB). These responses indicate client-side errors, such as requests for resources that do not exist or are forbidden. Monitoring this metric is essential for identifying issues that may affect user experience and application accessibility.


# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: HTTPCode_Backend_4XX
* <b>Namespace</b>: AWS/ELB
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: HTTPCode Backend 4XX

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Define the time range to analyze data points, useful for historical analysis or recent monitoring. Default time range is the last 24 hours.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: Useful for observing general trends in client-side error rates over time.
  * <b>Sum</b>: Shows the total count of 4XX responses from backend instances within the specified period.
  * <b>Minimum</b>: Indicates the lowest number of 4XX responses, revealing times with minimal client-side errors.
  * <b>Maximum</b>: Highlights peak counts of 4XX responses, which may signal recurring issues with client requests.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring to catch high error rates quickly.
    * <b>3600 seconds</b> for broader analysis of error trends over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Monitoring Client-Side Errors <a name="example-1"></a>

Track 4XX responses to identify and resolve issues such as broken links or incorrect API requests, improving overall user experience.


## Use Case 2: Troubleshooting Application Accessibility <a name="example-2"></a>
Monitor for spikes in 4XX responses to diagnose problems with user access to specific resources or endpoints, enabling timely corrections to application configurations.



# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/elasticloadbalancing/latest/classic/elb-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html