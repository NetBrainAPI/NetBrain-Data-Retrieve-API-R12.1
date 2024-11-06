# Table of Contents
- [Introduction](#introduction)

# Introduction <a name="introduction"></a>
An Amazon EBS volume is a durable, block-level storage device that we can attach to ec2instances. The API <b>Describe EBS</b> Volume will provide the list of EBS Volumes you have in the region. This API will provide details of each EBS volume such as attachment information, size, volume type etc.



This API is belongs to AWS VPC Router in NetBrain and uses describe_volume function of AWS rest api.



For more details about the AWS REST API, please refer to the following document: https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/ec2/client/describe_volumes.html