# Terraform-ec2

website:
https://learn.hashicorp.com/tutorials/terraform/aws-destroy?in=terraform/aws-get-started

part1 - Build Infrastructure:
add a file name "main.tf"
configare a EC2 aws 


past 2 - Change Infrastructure:
change the ami from amzon linux 2 --> ubuntu 16.02
line 17
before:
ami = "ami-830c94e3"
after:
ami = "ami-08d70e59c07c61a3a"


part 3 - Destroy Infrastructure:
in the terminal, write the command: 
terraform destroy 


part 4 - Define input Variables
added a new file name : "variables.tf" 
changed in main line 21
before:
Name = "ExampleAppServerInstance"
after:
Name = var.instance_name
I did apply for the changes with the command: 
$ terraform apply -var "instance_name=YetAnotherName"


part 5 -  Query Date with Outputs:
added a new file name: "outputs.tf"
define outputs for your EC2 instance's ID and IP address

part 6 - store remote state