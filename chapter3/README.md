# Chapter 3

This chapter contains Terraform examples focused on organizing infrastructure code.  
It includes examples of file layouts, environment separation, and workspaces.

The goal is to demonstrate best practices for:
- Structuring Terraform projects
- Separating environments (global vs. stage)
- Using workspaces for managing multiple deployments
These patterns help improve maintainability and scalability as infrastructure grows.

Explore the examples below and run each one independently.

## File Layout Example
- [global/s3](./file-layout-example/global/s3/)
- [stage/data-stores/mysql](./file-layout-example/stage/data-stores/mysql/)
- [stage/services/webserver-cluster](./file-layout-example/stage/services/webserver-cluster/)

## Workspaces Example
- [one-instance](./workspaces-example/one-instance/)

Each directory includes its own Terraform configuration and README.

To run any example:
```bash
terraform init
terraform plan
terraform apply
terraform destroy
```