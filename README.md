# Deploy code in S3 to EC2 instance using AWS CodeDepoy and AWS Code Pipeline

##### This project involves an S3 bucket, a pipeline, a code deploy application, and an ec2 instance. The goal of this workload is to successfully deploy a working code from an s3 bucket to an ec2 instance. 

# Core Resources 
##### S3 bucket - Used as a container to hold the source code. 
##### AWS Code Pipeline - This resource is used t pull the source code from the s3 bucket and deliver to AWS Code Deploy
##### AWS Code Deploy - This resource is sued to deploy the source code pulled by AWS Code Pipeline to an EC2instance. 

# Other resources created - 

#####  A role that contains the following policies 
1. AmazonEC2RoleforAWSCodeDeploy
2. AmazonSSMManagedInstanceCore
#####  This role contains policies that authenticate and permit ec2 instances to download code from s3 and access SSM that would be used by Code Deploy to install the application via ssh on an EC2 instance. 

AmazonEC2RoleforAWSCodeDeploy		
AmazonSSMManagedInstanceCore
AmazonCodeDeployRole - This role contains policies that provides CodeDeploy service access to expand tags and interact with Auto Scaling on your behalf.


# How To


