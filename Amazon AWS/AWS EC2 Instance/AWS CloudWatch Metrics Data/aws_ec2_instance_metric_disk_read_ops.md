# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Data-Intensive Workloads](#example-1) 
    - [Use Case 2 -- Overprovisioned or underprovisioned Instances](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>DiskReadOps</b> is a metric that measures the number of read operations performed on all storage devices attached to an EC2 instance in a specified period. It helps identify I/O bottlenecks, optimize instance sizing, and troubleshoot performance issues related to disk read operations.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: DiskReadOps
* <b>Namespace</b>: AWS/EC2
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: Disk Read Operations

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points. This is useful for historical analysis or monitoring recent trends. Default time range is last 24 hours.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: The average number of completed read operations from all instance store volumes attached to an EC2 instance. 
  * <b>Sum</b>: The sum of completed read operations from all instance store volumes attached to an EC2 instance.
  * <b>Minimum</b>: The minimum number of completed read operations from all instance store volumes attached to an EC2 instance.
  * <b>Maximum</b>: The maximum number of completed read operations from all instance store volumes attached to an EC2 instance.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Data-Intensive Workloads <a name="example-1"></a>
For applications that process large amounts of data, high DiskReadOps can signal potential bottlenecks. This could be due to inefficient data access patterns, insufficient storage performance, or network latency.

## Use Case 2: Overprovisioned or underprovisioned Instances <a name="example-2"></a>
If an instance consistently has low or high DiskReadOps, it may be overprovisioned or underprovisioned in terms of storage or I/O performance. Downsizing / upsizing the instance can help reduce costs without impacting performance.

# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/viewing_metrics_with_cloudwatch.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html