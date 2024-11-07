# Table of Contents
- [Introduction](#introduction)


# Introduction <a name="introduction"></a>
In AWS, a Direct Connect Virtual Interface (VIF) is a logical connection that enables you to access AWS services using a dedicated network connection provided by AWS Direct Connect.



The <b>Describe Direct Connect Virtual Interface</b> API in AWS Direct Connect is used to retrieve information about one or more virtual interfaces. This API can return details about both private and public virtual interfaces, providing insights into their configurations and statuses. The API response includes vlan, bgp asn, bgp neighbour state etc.

This API is integrated into the AWS DX router in NetBrain. It corresponds with the `describe_virtual_interfaces` function of the AWS REST API.



For more details about the AWS rest API, please check the AWS official document: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/directconnect/client/describe_virtual_interfaces.html