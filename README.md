# Deploy code in S3 to EC2 instance using AWS CodeDepoy and AWS Code Pipeline

![Deploy code in S3 to EC2 instance using AWS CodeDepoy and AWS Code Pipeline](https://github.com/blackxavier/code-deploy-test/blob/main/code-deploy.jpg "Deploy code in S3 to EC2 instance using AWS CodeDepoy and AWS Code Pipeline")

This project involves an S3 bucket, a pipeline, a code deploy application, and an ec2 instance. The goal of this workload is to successfully deploy a working code from an s3 bucket to an ec2 instance. 

# Core Resources 
 __S3 bucket__ - Used as a container to hold the source code. 
 __AWS Code Pipeline__ - This resource is used to pull the source code from the S3 bucket and deliver to AWS Code Deploy
 __AWS Code Deploy__ - This resource is sued to deploy the source code pulled by AWS Code Pipeline to an EC2instance. 

# Other resources created - 

Create a role that with the following policies.

``` AmazonEC2RoleforAWSCodeDeploy ```
``` AmazonSSMManagedInstanceCore ```

 This role contains policies that authenticate and permit ec2 instances to download code from s3 and access SSM that would be used by Code Deploy to install the application via ssh on an EC2 instance. 

Create a second role with the folowing policies . 
```` AmazonCodeDeployRole ````



# How To

1. Create S3 bucket
 2. Create a role (You can name it anything) and attach the following policies

     ```` AmazonEC2RoleforAWSCodeDeploy ````
        ```` AmazonSSMManagedInstanceCore ````

    Also create another role and attach the following policies

      ```` AmazonCodeDeployRole ````
3. Create an EC2 instance and attach the first role as an instance profile. 

4. Create an AWS CodeDeploy application
5. Create an AWS Code pipeline. 

Application is deployed successfully. 

 This is a short description of this workload,  you can find a more detialed tutorial on this detailed - [blog post](https://medium.com/@GeorgeBaidooJr/ci-cd-pipeline-deploy-a-simple-application-to-an-aws-ec2-instance-via-codedeploy-9fe0fb8f7130 )


