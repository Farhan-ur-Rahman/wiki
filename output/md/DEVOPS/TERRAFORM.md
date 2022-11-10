---
{}
---
   
**#Terraform AWS**   
   
     
   
to create a instance in AWS using terraform we have to use visual studio to write code in it.   
   
     
   
first link your AWS account into your machine and then \   
   
     
   
 make a folder in the VS and make a new file in it as main.TF   
   
     
   
write code as   
   
     
   
# Create a new instance of the latest Ubuntu 14.04 on an   
   
# t2.micro node with an AWS Tag naming it "HelloWorld"   
   
     
   
provider "aws" {   
   
  region = "us-west-2"   
   
}   
   
     
   
resource "aws_instance" "web" {   
   
  ami           = "${data.aws_ami.ubuntu.id}"   
   
  instance_type = "t2.micro"   
   
     
   
  tags = {   
   
    Name = "HelloWorld"   
   
  }   
   
}     
   
     
   
TERRAFORM INIT    
   
     
   
TERRAFORM PLAN    
   
     
   
TERRAFORM APPLY