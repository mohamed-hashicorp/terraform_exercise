# S3 Remote State Example

This folder contains example [Terraform](https://www.terraform.io/) configuration that create an 
[S3](https://aws.amazon.com/s3/) bucket and [DynamoDB](https://aws.amazon.com/dynamodb/) table in an 
[Amazon Web Services (AWS) account](http://aws.amazon.com/). The S3 bucket and DynamoDB table can be used as a 
[remote backend for Terraform](https://www.terraform.io/docs/backends/).

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

- Change the directory to chapter3/file-layout-example/global/s3
```
cd chapter3/file-layout-example/global/s3
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
- When prompted, enter the values of the S3 bucket and the DynamoDB table names
```
Note: You didn't use the -out option to save this plan, so Terraform can't guarantee to take exactly these actions if you run "terraform apply" now.
mohamedayman@mohameds-mbp s3 % terraform apply
var.bucket_name
  The name of the S3 bucket. Must be globally unique.

  Enter a value: terraform-up-and-running-bucket-mohamed

var.table_name
  The name of the DynamoDB table. Must be unique in this AWS account.

  Enter a value: terraform-up-and-running-dynamodb-mohamed
```
- Type yes if you prompted the following
```

Plan: 5 to add, 0 to change, 0 to destroy.

Changes to Outputs:
  + dynamodb_table_name = "terraform-up-and-running-dynamodb-mohamed"
  + s3_bucket_arn       = (known after apply)

Do you want to perform these actions?
  Terraform will perform the actions described above.
  Only 'yes' will be accepted to approve.

  Enter a value: yes
```

## Check was created
- To check your created S3, open your browser.
- Login to your [AWS console](https://aws.amazon.com/console) with your AWS credentials.
- In the search bar at the top, type S3 and click on it.
- You can see the deployed S3 bucket.
- In the search bar at the top, type Dynamodb and click on it.
- You can see the deployed Dynamodb table.


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