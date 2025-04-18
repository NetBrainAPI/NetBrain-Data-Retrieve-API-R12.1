# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- I/O Bound Applications](#example-1) 
    - [Use Case 2 -- Database Performance](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>DiskReadBytes</b> is a metric that measures the total number of bytes read from all storage devices attached to an EC2 instance in a specified period. It helps identify I/O bottlenecks, optimize instance sizing, and troubleshoot performance issues related to disk read operations.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: DiskReadBytes
* <b>Namespace</b>: AWS/EC2
* <b>Unit</b>: Bytes
* <b>Display Name in NetBrain</b>: Disk Read Bytes

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points. This is useful for historical analysis or monitoring recent trends. Default time range is last 24 hours.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: The average amount of bytes read from all instance store volumes attached to an EC2 instance within a specified period.
  * <b>Sum</b>: The sum of the amount of bytes read from all instance store volumes attached to an EC2 instance within a specified period.
  * <b>Minimum</b>: The minimum of the amount of bytes read from all instance store volumes attached to an EC2 instance within a specified period.
  * <b>Maximum</b>: The maximum of the amount of bytes read from all instance store volumes attached to an EC2 instance within a specified period.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: I/O Bound Applications <a name="example-1"></a>
If an instance's CPU utilization is consistently low or high, it may be overprovisioned or underprovisioned. By downsizing to a smaller instance type, you can reduce costs without compromising performance.

## Use Case 2: Database Performance <a name="example-2"></a>
For database-driven applications, high DiskReadBytes can signify database performance issues, such as slow query execution or excessive disk I/O

# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/viewing_metrics_with_cloudwatch.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html