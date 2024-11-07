# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Capacity Management](#example-1) 
    - [Use Case 2 -- Operational Health Monitoring](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>HealthyHostCount</b> metric tracks the number of backend instances (hosts) registered with a Classic Load Balancer (CLB) that are considered healthy. An instance is marked as healthy if it passes the health checks configured for the load balancer. Monitoring this metric is crucial for ensuring that traffic is routed only to healthy instances, which helps maintain application performance and reliability.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: HealthyHostCount
* <b>Namespace</b>: AWS/ELB
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: Healthy Host Count

# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Define the time range to analyze data points, useful for historical analysis or recent monitoring. Default time range is the last 24 hours.
* <b>Statistics</b>: Default value is Average.
  * <b>Average</b>: Useful for observing trends in the number of healthy hosts over time.
  * <b>Sum</b>: Shows the total count of healthy hosts over the specified period.
  * <b>Minimum</b>: Indicates the lowest number of healthy hosts recorded, revealing times with optimal performance.
  * <b>Maximum</b>: Highlights peak counts of healthy hosts, which may indicate an optimal scaling situation.
* <b>Period</b>: Default value is 3600 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for real-time monitoring to quickly assess the availability of healthy instances.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Capacity Management <a name="example-1"></a>

Monitor the HealthyHostCount to ensure sufficient healthy instances are available to handle incoming traffic, aiding in scaling decisions.



## Use Case 2: Operational Health Monitoring <a name="example-2"></a>
Track the number of healthy hosts to identify when maintenance or troubleshooting may be necessary, ensuring consistent application availability.



# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/elasticloadbalancing/latest/classic/elb-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html