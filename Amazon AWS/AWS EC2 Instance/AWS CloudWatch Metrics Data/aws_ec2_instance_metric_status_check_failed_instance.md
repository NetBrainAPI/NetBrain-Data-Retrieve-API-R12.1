# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Early Detection of Issues](#example-1) 
    - [Use Case 2 -- Custom Recovery Scripts](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>StatusCheckFailed_Instance</b> is a metric that indicates whether an EC2 instance has failed its instance status check in the last minute. By monitoring this metric, you can proactively identify and address instance health issues, ensuring optimal performance and reliability.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: StatusCheckFailed_Instance
* <b>Namespace</b>: AWS/EC2
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: Instance Status Check Failed

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points. This is useful for historical analysis or monitoring recent trends. Default time range is last 24 hours.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: The average of the instance status check in the last minute with values 0 or 1.
  * <b>Sum</b>: The sum of the instance status check in the last minute with values 0 or 1.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Early Detection of Issues <a name="example-1"></a>
By monitoring this metric, we can proactively identify instances that are experiencing health issues before they impact your applications or services.

## Use Case 2: Custom Recovery Scripts <a name="example-2"></a>
We can create custom scripts or automation tools to automatically reboot or terminate unhealthy instances.

# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/viewing_metrics_with_cloudwatch.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html