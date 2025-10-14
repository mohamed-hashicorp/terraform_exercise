# Chapter 1 Why Terraform

In this chapter the author explains the following topics:
- What is DevOps?
- What is IAC?
- What are the benefits of IAC?
- How does Terraform work?

## What is DevOps
DevOps is a set of processes, ideas and techniques.
The goal of DevOps is to make the software delievry vastly more efficient.
There are 4 core values in the DevOps movement:
* Culture
* Automtion
* Measurment
* Sharing

## What is IAC
IAC stands for Infrastructure as a Code.
The idea of IAC is that you write and execute a code to define, deploy, update, or destory your infrastructure.

There are 5 categories of IAC tools:
* Adhoc scripts: Simple script to do a specific task such as Bash scripts.
* Configuration Management tools: Tools to automate configurations on servers inside your infrastructure such as Ansible, Chef, and Puppet.
* Server Templating tools: These tools allow for the creation of reusable “templates” that define a server's configuration such as Docker, Vagrant, Packer.
* Orchesteration tools: Automate and coordinate complex workflows across multiple systems such as Kubernetes.
* Provisioning tools: Tools used to deploy your infrastructure such as Terraform.

## Benefits of IAC
- Reproducibility & consistency: deploying the same configuration over and over yields identical results
- Version control & auditability: changes to infrastructure are tracked like code changes
- Safety via planning & diffing: you can preview what will change before applying it
- Automation & speed: reduces manual toil, human error, and accelerates deployments
- Collaboration & reviews: infrastructure changes can go through code review, testing, etc.

## How does Terraform works
- Terraform is an opensource tool created by Hashicorp and written in Go language.
- The Go code is compiled down to a single file called terraform
- Terraform binary makes API calls on your behalf with one or more provider and it knows how to make the API calls based on the configuration you create
- Terraform keeps state about the current deployed infrastructure to know what changes need to be made.