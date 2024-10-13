 Project Title: Using Latest AMI from SSM parameter store to create Windows EC2 instance.

Description: the goal of this project is to dynamically create windows ec2 using the latest Amazom Machine Image (Ami), that can be deployed from any region without hardcoding AMI ID to a region.

Template Structure:
    - instance type; variable with default value
    - keypair securely stored and retrieved from SSM Parameter store during deployment of windows server
    - LatestWindowsAmi; Configured to retrieve value of latest windows AMI ID from public parameter in SSM parameter store.
    -Security Group: Ensures RDP access on port 3389.
Resources: explicitely defines Ec2 instance configuration for windows operating system using latest AMI ID.
