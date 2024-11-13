# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Network Activity Monitoring](#example-1) 
    - [Use Case 2 -- Detecting Potential Bottlenecks](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>ConnectionEstablishedCount</b> metric tracks the total number of successful connections established through an AWS NAT Gateway. This metric provides insight into how many connection attempts result in successful connections, which is useful for understanding network activity and ensuring the NAT Gateway is efficiently handling connection requests.


# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: ConnectionEstablishedCount
* <b>Namespace</b>: AWS/NATGateway
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: Connection Established Count

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Define the time range to analyze data points, useful for historical analysis or recent monitoring. Default time range is the last 24 hours.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: Useful for observing trends in successfully established connections over time.
  * <b>Sum</b>: Shows the total number of successfully established connections within the specified period.
  * <b>Minimum</b>: Indicates the lowest count of successful connections recorded, revealing times of low network activity.
  * <b>Maximum</b>: Highlights peak counts of successful connections, which may identify times of highest network load.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring to assess connection success rates promptly.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Network Activity Monitoring <a name="example-1"></a>
Monitor the ConnectionEstablishedCount to track successful connections, helping to gauge the NAT Gateway's effectiveness in handling requests and overall network activity.

## Use Case 2: Detecting Potential Bottlenecks <a name="example-2"></a>
Observe trends in successful connections to identify periods where additional resources may be required, ensuring seamless handling of connection requests.


# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/vpc/latest/userguide/metrics-dimensions-nat-gateway.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html