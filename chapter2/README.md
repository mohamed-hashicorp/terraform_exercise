# Chapter 2

This chapter contains several Terraform examples that build on each other.  
Each subdirectory demonstrates a different Terraform concept or feature.

The goal is to explore Terraform step by step — starting from creating a single server and progressing toward more advanced configurations using variables and multiple resources.

Browse the examples below and run each one independently:

- [one-server](./one-server/)
- [one-webserver](./one-webserver/)
- [one-webserver-with-vars](./one-webserver-with-vars/)
- [webserver-cluster](./webserver-cluster/)

Each directory includes:
- Its own `main.tf`
- A dedicated `README.md`


To run any example:
```bash
terraform init
terraform plan
terraform apply
terraform destroy
```