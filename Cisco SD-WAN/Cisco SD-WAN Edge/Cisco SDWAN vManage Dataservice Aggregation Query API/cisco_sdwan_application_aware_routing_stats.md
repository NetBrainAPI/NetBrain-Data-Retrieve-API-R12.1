# Table of Contents
- [Overview](#overview)
- [URL Format](#url-format)
- [User-Defined Parameters](#user-defined-parameters)
- [Data Query Rules](#data-query-rules)
- [Data Query Fields](#data-query-fields)
- [Data Query Metrics](#data-query-metrics)
- [Reference](#reference)

# Overview <a name="overview"></a>
This API is used to retrieve the application aware routing (AAR) stats of the device.

# URL Format <a name="url-format"></a>
* /dataservice/statistics/approute/aggregation?query={query}


# User-Defined Parameters <a name="user-defined-parameters"></a>
* N/A

# Data Query Rules <a name="data-query-rules"></a>
* <b>entry_time</b>: last_n_hours
  * <b>value</b>: 4
* <b>vmanage_system_ip</b>: in
  * <b>value</b>: <<device_id>>


# Data Query Metrics <a name="data-query-fields"></a>
* name
* remote_system_ip
* src_ip
* dst_ip
* local_color
* state
* src_port
* dst_port
* tunnel_color

# Data Query Metrics <a name="data-query-metrics"></a>
* <b>vqoe_score</b>: avg
* <b>jitter</b>: avg
* <b>latency</b>: avg
* <b>loss_percentage</b>: avg


# Reference <a name="reference"></a>
* https://developer.cisco.com/docs/sdwan/sd-wan-vmanage-v20-16/