Project Title: Lauch Ec2 instance in us-east-1 using infrastructure as a code (cloudformation).

Description: the purpose of this project is to create a dynamic cloudformation template, that can deploy an EC2 resources from multiple region by utilizing mapping features for Amazon Machine Image (AMI). This deployment will consider the use of security features to protect critical data like keypair.

Template Structures:
1. Parameters	
  MyInstanceType: 
    -Allows variable instance type with default value identified. this allows for flexibilty of use.
  MyKeypair:
    - This was securely provisioned using SSMParameter Store; critical data will be retrieved securely during deployment
  Mappings:
    - AMI IDs were mapped to different regions; us-east-1, us-west-1, eu-west-1, etc.
2. Resources:
    - Structured to dynamically retrieve AMI ID from region of deployment.