# Chapter 2 - Server Example

This folder contains an example [Terraform](https://www.terraform.io/) configuration that deploys a single server (using 
[EC2](https://aws.amazon.com/ec2/)) in an [Amazon Web Services (AWS) account](http://aws.amazon.com/). 

What we will do?

- Check pre-requisites
- Clone repo
- Create infrastructure
- Check what has been created
- Delete infrastructure


For more info, please see Chapter 2, "Getting started with Terraform", of 
*[Terraform: Up and Running](http://www.terraformupandrunning.com)*.

## Check Prerequistes

This guide was executed on MacOS so it assumes the following:
- You have Git installed.
- AWS Credentials are configured.
- Terraform is installed (I used Terraform 1.5.7)


## Clone repo
- Clone the Github repo by running the below command
```
git clone https://github.com/mohamed-hashicorp/terraform_exercise.git
```

- Change the directory to Deploying_a_single_server
```
cd Chapter2/deploying_a_cluster_web_servers
```

## Create Infrastructure
- Run Terraform init
```
terraform init
```

- Run Terraform apply
```
terraform apply
```

- Type yes if you prompted the following
```
Plan: 1 to add, 0 to change, 0 to destroy.

Changes to Outputs:
  + public_ip = (known after apply)

Do you want to perform these actions?
  Terraform will perform the actions described above.
  Only 'yes' will be accepted to approve.

  Enter a value: 
```


## Check was created
- To check your created server, open your browser.
- Login to your [AWS console](https://aws.amazon.com/console) with your AWS credentials.
- In the search bar at the top, type EC2 and click on it.
- Under Instances, click Instances (Running)
- You can see the deployed server.


## Delete Infrastructure
- When done, you can remove the resources with terraform destroy, type:
```
terraform destroy
```
- Type yes, when prompted:
```
    Do you really want to destroy all resources?
    Terraform will destroy all your managed infrastructure, as shown above.
    There is no undo. Only 'yes' will be accepted to confirm.
    Enter a value: 
```
- Once the resources are destoryed you will see:
```
Destroy complete! Resources: 1 destroyed
```