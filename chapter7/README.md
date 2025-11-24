# Chapter 7

This chapter contains advanced Terraform examples focused on:
- Kubernetes deployments (local and EKS)
- Multi-account and multi-region Terraform architectures
- Modular infrastructure patterns for Kubernetes, data stores, and multi-account setups
- Live environment structures using stage and prod

This chapter ties together modular design, multi-environment patterns, and Kubernetes orchestration.

Browse the examples below and run each independently.

---

## Examples
High-level Terraform examples showcasing different architectures:
- [kubernetes-eks](./examples/kubernetes-eks/)
- [kubernetes-local](./examples/kubernetes-local/)
- [multi-account-module](./examples/multi-account-module/)
- [multi-account-root](./examples/multi-account-root/)
- [multi-region](./examples/multi-region/)
- [single-account](./examples/single-account/)

---

## Live Environments
Environment-specific infrastructure for stage and prod:
- [live/prod/mysql](./live/prod/data-stores/mysql/)
- [live/stage/mysql](./live/stage/data-stores/mysql/)

---

## Modules
Reusable modules for data stores, multi-account structures, and Kubernetes services:
- [modules/data-stores/mysql](./modules/data-stores/mysql/)
- [modules/multi-account](./modules/multi-account/)
- [modules/services/eks-cluster](./modules/services/eks-cluster/)
- [modules/services/k8s-app](./modules/services/k8s-app/)

---

Each directory includes its own Terraform configuration and README.

To run any example:
```bash
terraform init
terraform plan
terraform apply
terraform destroy
```