# Terraform workspaces example

This folder contains an example [Terraform](https://www.terraform.io/) configuration that deploys a single server 
(using [EC2](https://aws.amazon.com/ec2/) and [Auto Scaling](https://aws.amazon.com/autoscaling/)). The point of this
example is to be a playground for [Terraform Workspaces](https://www.terraform.io/docs/state/workspaces.html), so the
configuration of the server will change depending on what workspace you're in. 

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

- Change the directory to workspaces-example/one-instance
```
cd chapter3/workspaces-example/one-instance
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

Do you want to perform these actions?
  Terraform will perform the actions described above.
  Only 'yes' will be accepted to approve.

  Enter a value: 
```
- List the current workspace
```
terraform workspace show
```
- Create a new workspace
```
terraform workspace new example1
```
- Run Terraform apply with auto-approve option to automatically start deploying the infrastructure without using prompt for confirmation.
```
terraform apply --auto-approve
```
- Create a new workspace
```
terraform workspace new example2
```
- Run Terraform apply with auto-approve option to automatically start deploying the infrastructure without using prompt for confirmation.
```
terraform apply --auto-approve
```

## Check was created
- To check your created server, open your browser.
- Login to your [AWS console](https://aws.amazon.com/console) with your AWS credentials.
- In the search bar at the top, type EC2 and click on it.
- Under Instances, click Instances (Running)
- You can see the deployed servers.
- Each EC2 instance is running separatly with a different state file.
- Note that the instance type of each deployed EC2 instance


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

