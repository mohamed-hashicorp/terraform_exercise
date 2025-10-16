# Chapter2 - Deploying a Single Server

In this section the author demonstrates on how to deploy a single server on AWS

## Prerequistes
This guide was executed on MacOS so it assumes the following:
- You have Git installed.
- AWS Credentials are configured.
- Terraform is installed (I used Terraform 1.5.7)

## Steps to follow this guide
- Clone the Github repo by running the below command
```
git clone https://github.com/mohamed-hashicorp/terraform_exercise.git
```
- Change the directory to Deploying_a_single_server
```
cd Chapter2/Deploying_a_single_server
```
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
- If finished this excersice, delete your infrastructure
```
terraform destroy
```
