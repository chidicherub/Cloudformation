Project Title: Deploy Basic Postgres RDS Database using Cloudformation and SSM Parameter Store.

Description: The goal of this lab is to securely deploy a PostgreSQL RDS that is not publicly accesible, using cloudformation template. Critical data like password and username will be stored and retrieved from SSM Parameter store. The template will be configured using important parameters, such as; DBName, DBInstanceIdentifier, DBSecurityGroup,MasterUsername, etc. 


Template Structure:
•	Parameters: Defines parameters for 
    -database name
    -Password; using SSM parameter store
    - Username; using SSM Parameter store
    - Database Subnet
    - Database Security Group
    - Multi AZ
    
•	Resources: configured to deploy an RDS instance on a securely using AWS intrinsic tool (!Ref) to fetch critical data from SSM parameter Store.