# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Capacity Management](#example-1) 
    - [Use Case 2 -- Cost Control in Multi-Subnet Architectures](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>NetworkAddressUsage</b>  metric in AWS CloudWatch tracks the number of IP addresses currently in use within a specific subnet in an Amazon Virtual Private Cloud (VPC). Monitoring this metric helps manage IP address allocation within subnets to prevent address exhaustion.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: NetworkAddressUsage
* <b>Namespace</b>: AWS/EC2
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: VPC Network Address Usage

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points. This is useful for historical analysis or monitoring recent trends. Default time range is last 24 hours.
* <b>Statistics</b>: Default value is Sum
  * <b>Average</b>: Average number of IP addresses in use over a period.
  * <b>Sum</b>: Total number of IP addresses used within a specific time frame.
  * <b>Minimum</b>: Minimum number of IP addresses in use during the time period.
  * <b>Maximum</b>: Helps identify peak usage moments, which may indicate high traffic loads.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring
    * <b>3600 seconds</b> for broader trend analysis over longer durations

# Use Cases Example <a name="example"></a>
## Use Case 1: Capacity Management <a name="example-1"></a>

Monitor IP usage to predict when a subnet may need more addresses, ensuring sufficient capacity for scaling.

## Use Case 2: Cost Control in Multi-Subnet Architectures <a name="example-2"></a>
Monitor IP address consumption across subnets to manage resources efficiently and prevent overspending.


# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/vpc/latest/userguide/network-address-usage.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html