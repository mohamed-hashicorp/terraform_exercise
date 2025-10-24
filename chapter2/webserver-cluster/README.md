# Web Server Example

This folder contains an example [Terraform](https://www.terraform.io/) configuration that deploys a cluster of web servers 
(using [EC2](https://aws.amazon.com/ec2/) and [Auto Scaling](https://aws.amazon.com/autoscaling/)) and a load balancer
(using [ELB](https://aws.amazon.com/elasticloadbalancing/)) in an [Amazon Web Services (AWS) 
account](http://aws.amazon.com/). The load balancer listens on port 80 and returns the text "Hello, World" for the 
`/` URL.

For more info, please see Chapter 2, "Getting started with Terraform", of 
*[Terraform: Up and Running](http://www.terraformupandrunning.com)*.

What we will do?

- Check pre-requisites
- Clone repo
- Create infrastructure
- Check what has been created
- Delete infrastructure


## Check Prerequistes

This guide was executed on MacOS so it assumes the following:
- You have Git installed.
- AWS Credentials are configured.
- Terraform is installed.


Please note that this code was written for Terraform 1.5.7


## Clone repo
- Clone the Github repo by running the below command
```
git clone https://github.com/mohamed-hashicorp/terraform_exercise.git
```

- Change the directory to webserver-cluster
```
cd Chapter2/webserver-cluster
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
Plan: 2 to add, 0 to change, 0 to destroy.

Changes to Outputs:
  + public_ip = (known after apply)

Do you want to perform these actions?
  Terraform will perform the actions described above.
  Only 'yes' will be accepted to approve.

  Enter a value: 
```

## Check was created

- When the `apply` command completes, it will output the hostname of the application load balancer. To test that IP:

```
curl http://(alb_dns_name)/
```
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
Destroy complete! Resources: 8 destroyed
```