# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Identify Vulnerable Instances](#example-1) 
    - [Use Case 2 -- Enforce IMDSv2 Usage](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>MetadataNoToken</b> is a metric that indicates the number of times an EC2 instance has accessed the Instance Metadata Service (IMDS) using the less secure IMDSv1 protocol. By monitoring this metric, you can identify instances that are vulnerable to security risks and take steps to mitigate them.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: MetadataNoToken
* <b>Namespace</b>: AWS/EC2
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: Metadata No Token

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points. This is useful for historical analysis or monitoring recent trends. Default time range is last 24 hours.
* <b>Statistics</b>: Default value is Sum.
  * <b>Sum</b>: The sum is the total number of times the Instance Metadata Service (IMDS) was accessed using the less secure IMDSv1 protocol within a specific time period.
  * <b>Percentile</b>: The percent value of the Instance Metadata Service (IMDS) was accessed using the less secure IMDSv1 protocol within a specific time period.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Identify Vulnerable Instances <a name="example-1"></a>
By monitoring this metric, you can identify instances that are vulnerable to potential security risks associated with IMDSv1.

## Use Case 2: Enforce IMDSv2 Usage <a name="example-2"></a>
We can take steps to configure your instances to require IMDSv2, such as using IAM Roles for Service Accounts or setting the HttpPutResponseHopLimit parameter.

# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/viewing_metrics_with_cloudwatch.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html