# Chapter 6

This chapter contains Terraform examples focused on:
- IAM roles and access control
- GitHub Actions OIDC authentication with AWS
- KMS encryption and customer-managed keys (CMKs)
- MySQL deployments with KMS and Secrets Manager
- Secure variable handling and encrypted credentials

This chapter builds skills for creating secure, production-grade Terraform infrastructure.

Explore the examples below and run each independently.

## IAM & Access Control
- [ec2-iam-role](./ec2-iam-role/)
- [github-actions-oidc](./github-actions-oidc/)

## Encryption & KMS
- [kms-cmk](./kms-cmk/)
- [mysql-kms](./mysql-kms/)

## Secrets Management
- [mysql-aws-secrets-mgr](./mysql-aws-secrets-mgr/)
- [mysql-vars](./mysql-vars/)

Each folder includes its own Terraform configuration and README.

To run any example:
```bash
terraform init
terraform plan
terraform apply
terraform destroy
```