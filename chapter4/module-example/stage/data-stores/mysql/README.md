# MySQL on RDS example (staging environment)

This folder contains an example [Terraform](https://www.terraform.io/) configuration that deploys a MySQL database  (using 
[RDS](https://aws.amazon.com/rds/) in an [Amazon Web Services (AWS) account](http://aws.amazon.com/). 

For more info, please see Chapter 4, "How to Create Reusable Infrastructure with Terraform Modules", of 
*[Terraform: Up and Running](http://www.terraformupandrunning.com)*.

What we will do?

- Check pre-requisites
- Clone repo
- Create webservers
- Check what have been created
- Delete infrastructure



## Check Pre-requisites
This guide was executed on MacOS so it assumes the following:
- You have Git installed.
- AWS Credentials are configured.
- Terraform is installed (I used Terraform 1.5.7)

## Clone repo
- Clone the Github repo by running the below command
```
git clone https://github.com/mohamed-hashicorp/terraform_exercise.git
```

- Change the directory to chapter4/module-example/stage/data-stores/mysql
```
cd chapter4/module-example/stage/data-stores/mysql
```
## Create Database
- Configure the database credentials as environment variables:
```
export TF_VAR_db_username=(desired database username)
export TF_VAR_db_password=(desired database password)
```

- Open `main.tf`, uncomment the `backend` configuration, and fill in the name of your S3 bucket, DynamoDB table, and the path to use for the Terraform state file.

- Deploy the database
```
terraform init
terraform apply
```

## Next Steps
- Once the database is deployed go to [webserver-cluster](../../services/webserver-cluster/) directory to continue deploying the webservers

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
