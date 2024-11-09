# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Database-Intensive Applications](#example-1) 
    - [Use Case 2 -- Data-Intensive Workloads](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>EBSReadBytes</b> is a metric that measures the total number of bytes read from all Elastic Block Store (EBS) volumes attached to an EC2 instance in a specified period. It helps identify I/O bottlenecks and optimize instance sizing for database-driven and data-intensive workloads.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: EBSReadBytes
* <b>Namespace</b>: AWS/EC2
* <b>Unit</b>: Bytes
* <b>Display Name in NetBrain</b>: EBS Read Byte

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points. This is useful for historical analysis or monitoring recent trends. Default time range is last 24 hours.
* <b>Statistics</b>: Default value is Average.
  * <b>Average</b>: The average number of bytes read from all EBS volumes attached to an EC2 instance in a specified period.
  * <b>Sum</b>: The sum of the number of bytes read from all EBS volumes attached to an EC2 instance in a specified period.
  * <b>Minimum</b>: The minimum number of bytes read from all EBS volumes attached to an EC2 instance in a specified period.
  * <b>Maximum</b>: The maximum number of bytes read from all EBS volumes attached to an EC2 instance in a specified period.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Database-Intensive Applications <a name="example-1"></a>
High EBSReadBytes can indicate that a database-driven application is experiencing performance issues due to excessive disk I/O. This could be caused by slow query execution, inefficient database indexing, or a large number of database connections.

## Use Case 2: Data-Intensive Workloads <a name="example-2"></a>
Applications that process large amounts of data, such as data warehouses and analytics pipelines, can have high EBSReadBytes. Monitoring this metric can help identify bottlenecks and optimize data access patterns.

# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/viewing_metrics_with_cloudwatch.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html