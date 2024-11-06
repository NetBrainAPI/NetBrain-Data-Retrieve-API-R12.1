# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Security Vulnerability Detection](#example-1) 
    - [Use Case 2 -- Configuration Compliance Auditing](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>DesyncMitigationMode_NonCompliant_Request_Count</b> metric tracks the number of requests handled by a Classic Load Balancer (CLB) that are considered non-compliant with the configured desynchronization mitigation mode settings. This metric is important for identifying requests that may bypass security measures designed to prevent desynchronization attacks, which can compromise backend instance performance and security. Monitoring this metric is essential for maintaining a secure and resilient application environment.


# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: DesyncMitigationMode_NonCompliant_Request_Count
* <b>Namespace</b>: AWS/ELB
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: Desync Mitigation Mode Non-Compliant Request Count

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Define the time range to analyze data points, useful for historical analysis or recent monitoring. Default time range is the last 24 hours.
* <b>Statistics</b>: Default value is Sum
  * <b>Average</b>: Useful for observing trends in non-compliant requests over time.
  * <b>Sum</b>: Shows the total count of non-compliant requests within the specified period.
  * <b>Minimum</b>: Indicates the lowest number of non-compliant requests recorded, revealing times with minimal issues.
  * <b>Maximum</b>: Highlights peak counts of non-compliant requests, which may indicate increased risk or configuration problems.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring to quickly detect increases in non-compliant requests.
    * <b>3600 seconds</b> for broader trend analysis over longer durations

# Use Cases Example <a name="example"></a>
## Use Case 1: Security Vulnerability Detection <a name="example-1"></a>

Monitor the DesyncMitigationMode_NonCompliant_Request_Count metric to identify requests that may expose the application to desynchronization attacks, enabling timely responses to potential threats.


## Use Case 2: Configuration Compliance Auditing <a name="example-2"></a>
Track non-compliant request counts to ensure that the CLB's desync mitigation settings are correctly configured and functioning as intended, thereby maintaining application security.




# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/elasticloadbalancing/latest/classic/elb-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html