# MySQL on RDS example

This folder contains an example [Terraform](https://www.terraform.io/) configuration that deploys a MySQL database (using 
[RDS](https://aws.amazon.com/rds/) in an [Amazon Web Services (AWS) account](http://aws.amazon.com/). 

What we will do?

- Check pre-requisites
- Clone repo
- Create infrastructure
- Check what has been created
- Delete infrastructure


For more info, please see Chapter 3, "How to Manage Terraform State", of 
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

- Change the directory to chapter3/file-layout-example/stage/data-stores/mysql
```
cd chapter3/file-layout-example/stage/data-stores/mysql
```

## Create Infrastructure
- Run Terraform init
```
terraform init
```
- When prompted, enter the S# bucket name and the state file path and the AWS region
```
Initializing the backend...
bucket
  The name of the S3 bucket

  Enter a value: terraform-up-and-running-bucket-mohamed

key
  The path to the state file inside the bucket

  Enter a value: global/s3/stage

region
  AWS region of the S3 Bucket and DynamoDB Table (if used).

  Enter a value: us-east-2
```  
- Run Terraform apply
```
terraform apply
```
- When prompted, enter the database password and username
```
var.db_password
  The password for the database

  Enter a value: 

var.db_username
  The username for the database

  Enter a value: 
```
- Type yes if you prompted the following
```
Plan: 1 to add, 0 to change, 0 to destroy.

Do you want to perform these actions?
  Terraform will perform the actions described above.
  Only 'yes' will be accepted to approve.

  Enter a value: 
```

## Check was created
- To check your created server, open your browser.
- Login to your [AWS console](https://aws.amazon.com/console) with your AWS credentials.
- In the search bar at the top, type RDS and click on it.
- Make sure that you in the correct region.
- You can see the deployed database.



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

