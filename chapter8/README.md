# Chapter 8

This chapter contains Terraform examples that go beyond typical declarative usage, including:
- External data sources
- Provisioners (local-exec and remote-exec)
- Null resources
It also includes a collection of small, reusable modules for building real infrastructure components such as load balancers, auto scaling groups, MySQL databases, and simple applications.


Browse and run each example independently.

---

## More Than Terraform
Examples showing how to extend Terraform with procedural logic:
- [external-data-source](./more-than-terraform/external-data-source/)
- [local-exec-provisioner](./more-than-terraform/local-exec-provisioner/)
- [null-resource](./more-than-terraform/null-resource/)
- [remote-exec-provisioner](./more-than-terraform/remote-exec-provisioner/)

---

## Small Modules — Examples
Pre-built examples using the small modules:
- [alb](./small-modules/examples/alb/)
- [asg](./small-modules/examples/asg/)
- [mysql](./small-modules/examples/mysql/)

---

## Small Modules — Live Environments
Stage and production deployments using the modules:
- [prod/mysql](./small-modules/live/prod/data-stores/mysql/)
- [prod/hello-world-app](./small-modules/live/prod/services/hello-world-app/)
- [stage/mysql](./small-modules/live/stage/data-stores/mysql/)
- [stage/hello-world-app](./small-modules/live/stage/services/hello-world-app/)

---

## Small Modules — Module Definitions
Reusable Terraform modules for infrastructure building blocks:
- [asg-rolling-deploy](./small-modules/modules/cluster/asg-rolling-deploy/)
- [mysql](./small-modules/modules/data-stores/mysql/)
- [alb](./small-modules/modules/networking/alb/)
- [hello-world-app](./small-modules/modules/services/hello-world-app/)

---

Each directory contains its own Terraform configuration and README.

To run any example:
```bash
terraform init
terraform plan
terraform apply
terraform destroy
```