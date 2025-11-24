# Chapter 4

This chapter introduces reusable Terraform modules and shows how to structure projects using modules across multiple environments (stage and prod).

The goal is to demonstrate:
- How to create modules for shared infrastructure logic
- How to reuse modules across environments
- How to organize production and staging environments cleanly
- How to separate concerns between modules and environment-specific configuration

These patterns are essential for scaling Terraform code in real-world teams.

Browse the examples below and explore module usage and environment structure.

## Module Definition
- [modules/services/webserver-cluster](./module-example/modules/services/webserver-cluster/)

## Stage Environment
- [stage/data-stores/mysql](./module-example/stage/data-stores/mysql/)
- [stage/services/webserver-cluster](./module-example/stage/services/webserver-cluster/)

## Production Environment
- [prod/data-stores/mysql](./module-example/prod/data-stores/mysql/)
- [prod/services/webserver-cluster](./module-example/prod/services/webserver-cluster/)

Each directory contains its own Terraform configuration and README.

To run any example:
```bash
terraform init
terraform plan
terraform apply
terraform destroy
```