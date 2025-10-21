# Chapter3 - How to Manage Terraform state

In this section the author demonstrates how isolate your infrastructure using workspace

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
cd chapter3/isolation_workspace
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
- Now run the following command to change workspace `terraform workspace new exmaple1`
- Run `terraform apply`
- Change the workspace again `terraform workspace new exmaple2`
- Check the S3 bucket to confirm that the isolation is done through workspaces. You should find separate directory inside the bucket for each workspace created.
- If finished this excersice, delete your infrastructure
```
terraform destroy
```
