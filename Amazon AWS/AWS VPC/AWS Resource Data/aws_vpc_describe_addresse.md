# Table of Contents
- [Introduction](#introduction)

# Introduction <a name="introduction"></a>
An Elastic IP address is associated with your AWS account. It's a public IP address, which is reachable from the internet.



The "Describe Elastic IP Addresses" API provides a list of Elastic IP addresses in your specified region. The API response includes details such as the public IP, private IP, attached ENI ID, and more.



This API is belongs to AWS VPC Router in NetBrain and uses describe_addresses function of AWS rest API of each Elastic IP address



For more details about the AWS REST API, please refer to the following AWS official document: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ec2/client/describe_addresses.html