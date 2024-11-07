# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Capacity Management](#example-1) 
    - [Use Case 2 -- Troubleshooting Connection Failures](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>ErrorPortAllocation</b> metric tracks the number of connection attempts through an AWS NAT Gateway that failed due to port allocation errors. This metric is crucial for identifying issues with NAT Gateway resource availability, as port allocation errors may occur when all available ports are in use, potentially indicating that the gateway is under heavy load or that additional resources are needed.


# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: ErrorPortAllocation
* <b>Namespace</b>: AWS/NATGateway
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: Error Port Allocation

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Define the time range to analyze data points, useful for historical analysis or recent monitoring. Default time range is the last 24 hours.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: Useful for observing trends in port allocation errors over time.
  * <b>Sum</b>: Shows the total count of port allocation errors within the specified period.
  * <b>Minimum</b>: Indicates the lowest count of port allocation errors recorded, helpful for understanding periods of stable performance.
  * <b>Maximum</b>: Highlights peak counts of port allocation errors, which may suggest times of high demand or insufficient resources.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring to detect immediate issues with port allocation.
    * <b>3600 seconds</b> for analyzing overall trends and resource needs over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Capacity Management <a name="example-1"></a>
Monitor the ErrorPortAllocation metric to identify times when the NAT Gateway is unable to allocate ports, helping to determine if additional NAT Gateways are needed to handle peak demand.

## Use Case 2: Troubleshooting Connection Failures <a name="example-2"></a>
Track port allocation errors to diagnose failed connections, enabling timely adjustments to resource allocation or connection configuration.

# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/vpc/latest/userguide/metrics-dimensions-nat-gateway.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html