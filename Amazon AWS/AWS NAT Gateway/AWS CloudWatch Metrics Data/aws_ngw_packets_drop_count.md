# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Network Performance Monitoring](#example-1) 
    - [Use Case 2 -- Capacity Planning](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>PacketsDropCount</b> metric tracks the number of packets dropped by an AWS NAT Gateway. This can occur due to various reasons, such as reaching capacity limits or encountering network issues. Monitoring this metric is essential for ensuring reliable network performance and for identifying potential connectivity or capacity problems that may affect applications relying on the NAT Gateway.


# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: PacketsDropCount
* <b>Namespace</b>: AWS/NATGateway
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: Packets Drop Count

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Define the time range to analyze data points, useful for historical analysis or recent monitoring. Default time range is the last 24 hours.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: Useful for observing trends in packet drops over time.
  * <b>Sum</b>: Shows the total count of dropped packets within the specified period.
  * <b>Minimum</b>: Indicates the lowest count of packet drops recorded, useful for understanding stable periods.
  * <b>Maximum</b>: Highlights peak packet drop counts, which may indicate times of network congestion or resource limitations.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring to detect packet drops as they occur.
    * <b>3600 seconds</b> for longer-term trend analysis to understand patterns in packet drop occurrences.

# Use Cases Example <a name="example"></a>
## Use Case 1: Network Performance Monitoring <a name="example-1"></a>
Monitor the PacketsDropCount metric to identify times of packet loss, enabling timely troubleshooting and ensuring consistent network performance.


## Use Case 2: Capacity Planning <a name="example-2"></a>
Track packet drop counts to determine if additional NAT Gateway resources are needed during high traffic periods, helping to prevent packet loss and maintain connectivity.

# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/vpc/latest/userguide/metrics-dimensions-nat-gateway.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html