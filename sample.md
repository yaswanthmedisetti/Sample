NODE SERVER SETUP 

CREATE SECURITY GROUP 

We now need to create security group for Node servers: 

![image](https://github.com/yaswanthmedisetti/Sample/assets/155810198/01750ddf-7238-4695-8eee-200fc68fbf42)

![image](https://github.com/yaswanthmedisetti/Sample/assets/155810198/f603d5e8-04ea-4470-aff0-101172387107)

Create  a tag for this security group. All resources for the SmartWinnr Production will be having the name tag = smartwinnr_node_prd_sec_grp 
CREATE NODE EC2 INSTANCE 

We will create 1 EC2 instance. Later on we will see how to create more instances from this one using autoscaling etc. 

EC2 IAM ROLE 

Since we want to spin other EC2 versions from this using autoscaling etc., we need to use an IAM role while creating the EC2 instance. Go to IAM->Roles. Create a new role EC2NodeUser. (No need to create for new Datacenter like Mumbai, already created). Attach “Mobillions3BackupPolicy” to this role. Now during EC2 instance creation, select this role. 

CREATE EC2 INSTANCE 

Check out CREATE APPROPRIATE EC2 INSTANCE section from Mobillion Amazon Deployment Guide. We just provide the high-level information here: 

Search and select CentOS7 from the Community AMI in Step 1 of launch instance. 

 Instance Details 
