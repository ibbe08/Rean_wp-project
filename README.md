# WordPress Chef Deployment in a VPC


# ABOUT

This template is a tool to automate the installation of a basic WordPress site using AWS CloudFormation.
The template sets up a VPC and all its components, an EC2 instance and uses CHEF to install WordPress on the instance.

# Stack creation walkthrough on AWS

Create a KeyPair in the region you want to deploy the stack.
https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/GettingStarted.Walkthrough.html
See step 2!

. Choose file to upload your template. Hit Next!



. Enter a Stack name and Parameters:
		DBpassord-DBUser-KeyPair





. Review and Hit  “Create”




. Stack Creation Processing






. Review Resources Tab when the process is completed




. View Stack Creation Events





. View WordPress URL in the Outputs Tab







# ADDITIONAL DOCUMENTATION

# Highly Available and Scalable WordPress on AWS

With AWS you can build a Multi_Tiered Architecture by including:

An Elastic Load Balancer to evenly distribute incoming traffic between the instances and perform Health checks on the instances. ELB works seamlessly with Auto Scaling Groups.
ELB is a managed service. No maintenance required.

An Auto Scaling Group to automatically scale out or down depending on workloads. Adding built in scalability and elasticity. Combined with the ELB, it can also automatically stop unhealthy instances and launch new ones, ensuring that the WP site does not go down for long periods of time.

An RDS Database with MySql engine, offering Read scalability with Read replicas (providing Read performance) and offloading the maintenance to AWS since it is a managed service as well. A DB security group will allow DB access only to the WP EC2 instances. Additionally you are billed on an hourly consumption.

S3, Route 53 and CloudFront for content delivery network to enhance performance and reduced latency. Delivering static assets, images and templates from the nearest edge locations.

CloudWatch to monitor the CPU, network utilization and send system alerts via SNS emails or SMS.

Security. With AWS security groups and IAM policies to manage user accounts.

https://supermarket.chef.io/cookbooks/wordpress-readme

https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/Welcome.html

https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-sample-templates.html

https://github.com/chef/chef

https://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/VPC_Introduction.html
