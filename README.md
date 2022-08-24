# Deploy a high-available web app using AWS CloudFormation 
In this project, it is required to deply infrastructure as shown in the fllowing image:
![AWSWebAppInfrastructure](https://github.com/MohamedSamiMohamed/Infrastructure-as-Code/blob/master/AWSWebAppInfrastructure.png)
as you can see, this includes:

1. **Internet gateway** for the users to access your resources through internet.
2. **VPC**
3. **Application Load Balancer** to route traffic and loadbalance it through EC2 instances
4. **security groups** to control the traffic comming in and out and secure it
5. **Elastic IP addresses** for making a reserved IP address given to :
6. **2 NAT GateWays** which are created in 2 different public subnets (for those subnets to be public we need to associate them with a public route table) , also note that they are in different availability zones , the reason why we create NAT GW is to be able to access our EC2 instances that are not publicly exposed ( in private subnet) which is a more secure way since our app is hosted in those instances
7. **Webserver security group** attached to the instances
8. **Autoscaling** for them and so target groups
