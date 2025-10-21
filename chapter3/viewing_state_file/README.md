# Chapter3 - How to Manage Terraform state

In this section the author explains the state file contents and what you will find in the state file incase if you deployed an EC2 instance on AWS


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
cd chapter3/viewing_state_file
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
- Check the terraform state file `terraform.tfstate` created in the same directory and confirm it has the same information that you have provided.
- If finished this excersice, delete your infrastructure
```
terraform destroy
```
