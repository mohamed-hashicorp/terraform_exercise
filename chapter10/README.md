# Chapter 910

This chapter covers how to test Terraform infrastructure code, including:
- Manual testing of Terraform modules and environments
- Automated testing using Terratest
- Writing integration tests, unit-style tests, and policy tests
- Structuring examples, modules, and live environments for testability

Browse and run each example independently.

---

## Examples
Self-contained Terraform examples used for learning, experimentation, and testing:
- [alb](./examples/alb/)
- [asg](./examples/asg/)

---

## Live Environments
Stage and production deployments used for real-world testing and validation:
- [prod/mysql](./live/prod/data-stores/mysql/)
- [prod/hello-world-app](./live/prod/services/hello-world-app/)
- [stage/mysql](./live/stage/data-stores/mysql/)
- [stage/hello-world-app](./live/stage/services/hello-world-app/)

---

## Modules
Reusable Terraform modules that can be tested independently or as part of environments:
- [asg-rolling-deploy](./modules/cluster/asg-rolling-deploy/)
- [mysql](./modules/data-stores/mysql/)
- [alb](./modules/networking/alb/)
- [hello-world-app](./modules/services/hello-world-app/)

---

## Tests
Automated tests implemented with Terratest:
- [Go test suite](./test/)
  - Example tests (ALB, ASG, MySQL, Hello World App)
  - Integration tests
  - OPA policy tests
  - Shared test helpers