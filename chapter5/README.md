# Chapter 5

This chapter contains advanced Terraform examples covering:
- Loops (`for_each`, `count`)
- Conditional logic (`if`, string directives)
- IAM automation
- Multi-environment infrastructure layouts
- Zero-downtime deployments and instance refresh patterns
- Reusable modules for both IAM and webserver clusters

The goal is to explore Terraform techniques used in real-world infrastructure:
- Creating multiple resources dynamically
- Writing more expressive, maintainable Terraform code
- Structuring live environments (stage/prod/global)
- Using modules for repeatable infrastructure
- Performing rolling updates without downtime

These examples build on earlier chapters and introduce more production-grade patterns.

Browse the examples below and run each one independently.

## Loops & If Statements
This section demonstrates dynamic resource creation, conditionals, and IAM workflows.
- [loops-and-if-statements/live](./loops-and-if-statements/live/)
- [loops-and-if-statements/modules](./loops-and-if-statements/modules/)

## Zero Downtime Deployment
This section demonstrates strategies for deploying updates without disruption.
- [zero-downtime-deployment/live](./zero-downtime-deployment/live/)
- [zero-downtime-deployment/modules](./zero-downtime-deployment/modules/)

Each directory contains its own Terraform configuration and README.

To run any example:
```bash
terraform init
terraform plan
terraform apply
terraform destroy
```