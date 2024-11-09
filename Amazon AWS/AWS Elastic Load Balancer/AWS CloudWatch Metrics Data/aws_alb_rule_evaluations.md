# Table of Contents
- [Overview](#overview)
- [Metric Info](#metric-info)
- [User-Defined Parameters](#user-defined-parameters)
- [Use Cases Example](#example)
    - [Use Case 1 -- Load Balancer Performance Analysis](#example-1) 
    - [Use Case 2 -- Troubleshooting Rule Configuration Issues](#example-2)
- [Reference](#reference)

# Overview <a name="overview"></a>
The <b>RuleEvaluations</b> metric tracks the number of rules evaluated by the load balancer when processing incoming requests. This count excludes the default rule and includes the first 10 rule evaluations per request at no additional cost. Tracking this metric can help understand how often the load balancer is evaluating rules to route traffic, which is useful for optimizing rule configurations and managing costs associated with complex routing logic.

# Metric Info <a name="metric-info"></a>
* <b>Metric Name</b>: RuleEvaluations   
* <b>Namespace</b>: AWS/ApplicationELB
* <b>Unit</b>: Count
* <b>Display Name in NetBrain</b>: Rule Evaluations


# User-Defined Parameters <a name="user-defined-parameters"></a>
* <b>Start Time / End Time</b>: Specify the time range for viewing data points. This is useful for historical analysis or monitoring recent trends. The default time range is the last 24 hours.
* <b>Statistics</b>: Default value is Sum.
  * <b>Average</b>: The average number of rule evaluations per request during the specified time period.
  * <b>Sum</b>: The total number of rule evaluations during the specified time period.
  * <b>Minimum</b>: The least number of rule evaluations in the selected period.
  * <b>Maximum</b>: The maximum number of rule evaluations in the selected period.
* <b>Period</b>: Default value is 300 second.
  * <b>Recommended Values</b>:
    * <b>300 seconds</b> for near real-time monitoring.
    * <b>3600 seconds</b> for broader trend analysis over longer durations.

# Use Cases Example <a name="example"></a>
## Use Case 1: Load Balancer Performance Analysis <a name="example-1"></a>
The Rule Evaluations metric can be used to understand how rule processing is impacting load balancer performance. A significant increase in rule evaluations could signal potential bottlenecks or inefficiencies in routing logic.

## Use Case 2: Troubleshooting Rule Configuration Issues <a name="example-2"></a>
If requests are being misrouted or taking longer than expected to process, high rule evaluation counts can help indicate rule misconfigurations. Reviewing the number of evaluations can pinpoint areas where rule logic can be simplified or adjusted.





# Reference <a name="reference"></a>
* <b>Metrics Details</b>: https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-cloudwatch-metrics.html
* <b>AWS CloudWatch Parameters</b>: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/cloudwatch/client/get_metric_data.html