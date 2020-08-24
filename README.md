# MediaWiki
mediawiki terraform

AWS Specifications :-

The AWS architecture consisits of 1 VPC and 3 subnets deployed in 3 different AZ's. The 3 EC2 instances of 2 Web and 1 DB are deployed among three AZ's. The Web Instances are behind a ELB with crosszone load balancing enabled. The listener port is configured to port 80. The healthcheck up also configured on port 80. The connection drainout parameter is set to 400.Dedicated security groups are created for webservers and db instance.

Terraform :- Update the values in the terraform.tfvars as per the requirement

AWS_ACCESS_KEY
AWS_SECRET_KEY
AMI_ID
AWS_REGION     = "us-west-2"
INSTANCE_TYPE  = "t2.micro"
AZS            = ["us-west-2a", "us-west-2b", "us-west-2c"]
AWS_CIDR_VPC   = "10.0.0.0/16"
AWS_CIDR_SUBNET1 = "10.0.1.0/24"
AWS_CIDR_SUBNET2 = "10.0.2.0/24"
AWS_CIDR_SUBNET3 = "10.0.3.0/24"
PATH_TO_PRIVATE_KEY = "mykey"
PATH_TO_PUBLIC_KEY = "mykey.pub"
INSTANCE_USERNAME = "centos"



Ansible Playbook that performs the following:

Performs the Installation of the MySQL Database
Creates the Database and Users and other Validations.
Role that installs Apache HTTPD, PHP 
Configures the MediaWiki webserver
Makes it ready for the Launch on the browser.

