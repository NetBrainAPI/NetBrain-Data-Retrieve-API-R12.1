# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 --  Early Detection of Hardware Issues](#example-1) 
    - [Use Case 2 -- Custom Recovery Scripts](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>StatusCheckFailed_System</b> is a CloudWatch metric that indicates whether an EC2 instance has failed its system status check in the last minute. A system status check assesses the health of the underlying EC2 hardware, such as the CPU, memory, and storage. If the system status check fails, it means there might be an issue with the hardware or the underlying infrastructure that could impact the instance's performance and reliability.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: StatusCheckFailed_System
* <b>Namespace</b>: AWS/EC2
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: System Status Check Failed

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points. This is useful for historical analysis or monitoring recent trends. Default time range is last 24 hours.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: The average value of system status checks done in the last minute.
  * <b>Sum</b>: The sum of system status checks done in the last minute.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1:  Early Detection of Hardware Issues <a name="example-1"></a>
By monitoring this metric, you can proactively identify instances that are experiencing underlying hardware problems.

## Use Case 2: Custom Recovery Scripts <a name="example-2"></a>
Some custom scripts to automate recovery actions, such as rebooting instances or terminating and replacing them can be created, based on the StatusCheckFailed_System metric.

# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/viewing_metrics_with_cloudwatch.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html