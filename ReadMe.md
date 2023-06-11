Welcome to my 3 Tier Architecture Demo.
Here I am going to create a web tier, app tier and database tier and connect them according to our requirements and trying to maintain the power of cloud such as Scalability, High Availability, Resiliency, and Security. 
WEB Tier:
APP Tier:
Database Tier

first i will be creating a VPC and 6 subnets in 2 AZs to ensure high availability.
Out of the 6 subnets, two subnets will be public subnets and the other four will be private.
so the public subnets, one from each AZ are going to face the internet users directly thus forming the presentation tier.
I will be using two private subnets, one from each AZ for the application tier to process/handle the data which comes from the presentation tier.
The remaining to private subnets are left for storage where the processed data will be stored. thus forming the data tier. 

we have to add internet traffic to our public subnets which is done by Internet Gateway 
Private subnets talk to internet through NAT Gateway
 
 Security Groups will be controlling the inbound rules and the Routing Tables helps to mange the flow through the subnets.
user data will help in installing the required software for the virtual machine we need.
