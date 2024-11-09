# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Target Health Monitoring](#example-1) 
    - [Use Case 2 -- Troubleshooting Target Issues](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>HTTPCode_Target_2XX_Count</b> metric counts the number of HTTP 2XX status code responses returned by the targets in the target group. These codes indicate that the request was successfully processed by the backend target. Monitoring this metric helps in assessing the overall health and performance of the target instances, ensuring that they respond appropriately to requests.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: HTTPCode_Target_2XX_Count   
* <b>Namespace</b>: AWS/ApplicationELB
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: HTTP Code Target 2XX Count

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: The average number of 2XX responses over the specified time period.
  * <b>Sum</b>: The total number of 2XX responses over the specified time period.
  * <b>Minimum</b>: The least number of 2XX responses during the selected period.
  * <b>Maximum</b>: The maximum number of 2XX responses during the selected period.
* <b>Period</b>: Default value is 300 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for near real-time monitoring.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Target Health Monitoring <a name="example-1"></a>
Track the HTTP Code Target 2XX Count metric to monitor the health of your backend targets. If this value is low or decreasing, it may indicate that targets are not processing requests correctly or there may be issues with the application code.





## Use Case 2: Troubleshooting Target Issues <a name="example-2"></a>
If you notice that the HTTP Code Target 2XX Count is abnormally low, use it as a signal to investigate the backend application for errors. Low or missing 2XX responses might indicate target application failures or misconfigurations.





# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html