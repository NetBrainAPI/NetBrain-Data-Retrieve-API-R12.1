# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Early Detection of Issues](#example-1) 
    - [Use Case 2 -- Preventive Maintenance](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>StatusCheckFailed</b> is a binary metric that indicates whether an EC2 instance has failed its status check in the last minute. By monitoring this metric, you can proactively identify and address potential issues with EC2 instances. This can help prevent service disruptions and improve overall system reliability.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: StatusCheckFailed
* <b>Namespace</b>: AWS/EC2
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: Status Check Failed

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points. This is useful for historical analysis or monitoring recent trends. Default time range is last 24 hours.
* <b>Statistics</b>: Default value is Average.
  * <b>Average</b>: The average value of status checks done in the last minute.
  * <b>Sum</b>: The sum of status checks done in the last minute.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Early Detection of Issues <a name="example-1"></a>
By monitoring this metric, you can proactively identify instances that are experiencing health issues before they impact your applications or services. This allows you to take timely corrective actions, such as restarting the instance or investigating the root cause of the issue.

## Use Case 2: Preventive Maintenance <a name="example-2"></a>
Automated actions or alerts can be setup to notify you when instances fail their status checks. This enables you to proactively address potential problems and prevent service outages.

# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/viewing_metrics_with_cloudwatch.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html