# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Traffic Load Management](#example-1) 
    - [Use Case 2 -- Identifying Usage Patterns](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>BytesProcessed</b> metric for VPC Endpoints measures the volume of data, in bytes, processed through a VPC Endpoint. This metric is valuable for understanding data transfer usage, monitoring network efficiency, and managing traffic flow through the endpoint.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: BytesProcessed
* <b>Namespace</b>: AWS/PrivateLinkEndpoints
* <b>Unit</b>: Bytes
* <b>Display Name in NetBrain</b>: Bytes Processed

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points, useful for historical analysis or monitoring recent trends. Default time range is last 24 hours.
* <b>Statistics</b>: Default value is Average.
  * <b>Average</b>: Provides a general view of data processing trends over the selected period.
  * <b>Sum</b>: Shows the cumulative amount of data processed within the specified time range.
  * <b>Minimum</b>: Highlights periods with minimal data usage.
  * <b>Maximum</b>: Identifies peak data usage moments.
* <b>Period</b>: Default value is 300 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Traffic Load Management <a name="example-1"></a>
Track <b>BytesProcessed</b> to monitor data flow through the VPC Endpoint, ensuring it aligns with expected traffic levels and prevents overloading.




## Use Case 2: Identifying Usage Patterns <a name="example-2"></a>
Use <b>BytesProcessed</b> to analyze data consumption trends over time, providing insights for future capacity planning and adjustments.

# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/vpc/latest/privatelink/privatelink-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html