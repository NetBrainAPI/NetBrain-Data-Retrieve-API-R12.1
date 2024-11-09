# Table of Contents
- [Introduction](#introduction)


# Introduction <a name="introduction"></a>
An EC2 (Elastic Compute Cloud) instance is a virtual server in the cloud offered by Amazon Web Services (AWS). It provides resizable compute capacity and allows you to run applications and services on the AWS infrastructure.



The <b>Describe EC2 Instance</b> API offers detailed information about the specific EC2. The response includes instance type, ami, IP address, etc.

This API is integrated into the AWS EC2 instance in NetBrain. It corresponds with the describe_instances function of the AWS REST API, using the `instance-id` filter to retrieve specific information.



For more details about the AWS rest API, Please refer to the following AWS official document: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ec2/client/describe_instances.html