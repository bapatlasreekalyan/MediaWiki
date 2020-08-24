# MediaWiki
mediawiki terraform

AWS Specifications :-

The AWS architecture consisits of 1 VPC and 3 subnets deployed in 3 different AZ's. The 3 EC2 instances of 2 Web and 1 DB are deployed among three AZ's. The Web Instances are behind a ELB with crosszone load balancing enabled. The listener port is configured to port 80. The healthcheck up also configured on port 80. The connection drainout parameter is set to 400.Dedicated security groups are created for webservers and db instance.

Terraform :- Update the values in the terraform.tfvars as per the requirement in terraform.tfvars file

Ansible Playbook that performs the following:

Performs the Installation of the MySQL Database
Creates the Database and Users and other Validations.
Role that installs Apache HTTPD, PHP 
Configures the MediaWiki webserver
Makes it ready for the Launch on the browser.

