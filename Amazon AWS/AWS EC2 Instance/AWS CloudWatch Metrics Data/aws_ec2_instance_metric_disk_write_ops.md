# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Log-Heavy Applications](#example-1) 
    - [Use Case 2 -- Overprovisioned or Underprovisioned Instances](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>DiskWriteOps</b> is a metric that measures the number of write operations performed on all storage devices attached to an EC2 instance in a specified period. It helps identify I/O bottlenecks, optimize instance sizing, and troubleshoot performance issues related to disk write operations.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: DiskWriteOps
* <b>Namespace</b>: AWS/EC2
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: Disk Read Operations

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points. This is useful for historical analysis or monitoring recent trends. Default time range is last 24 hours.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: The average of the number of completed write operations to all instance store volumes attached to an EC2 instance in a specified period.
  * <b>Sum</b>: The sum of the number of completed write operations to all instance store volumes attached to an EC2 instance in a specified period.
  * <b>Minimum</b>: The minimum of the number of completed write operations to all instance store volumes attached to an EC2 instance in a specified period.
  * <b>Maximum</b>: The maximum of the number of completed write operations to all instance store volumes attached to an EC2 instance in a specified period.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Log-Heavy Applications <a name="example-1"></a>
Applications that generate large amounts of log data can also have high DiskWriteOps. Monitoring this metric can help identify applications that are excessively writing to disk and may require optimization.

## Use Case 2: Overprovisioned or Underprovisioned Instances <a name="example-2"></a>
If an instance consistently has low DiskWriteOps, it may be overprovisioned or Underprovisioned in terms of storage or I/O performance. Downsizing or upsizing the instance can help reduce costs without impacting performance.

# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/viewing_metrics_with_cloudwatch.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html