```markdown
# Existing IAM User Example (Chapter 5)

This folder contains an example [Terraform](https://www.terraform.io/) configuration that references an **existing**
[IAM](https://aws.amazon.com/iam/) user in your [Amazon Web Services (AWS) account](https://aws.amazon.com/).

**The goal of this exercise is to learn how to import existing resources into Terraform state.**

---

## What We Will Do
- Check pre-requisites
- Clone the repo
- Identify an existing IAM user
- Import the IAM user into Terraform state
- Apply the configuration
- (Optional) Delete infrastructure

For more info, please see Chapter 5, **"Terraform Tips & Tricks: Loops, If-Statements, Deployment, and Gotchas"** of  
*Terraform: Up and Running* — <http://www.terraformupandrunning.com>

---

## Check Pre-requisites

This guide assumes:
- You have Git installed.
- AWS credentials are configured on your machine.
- Terraform 1.x is installed (example tested using Terraform 1.5.x).
- You already have an IAM user in your AWS account that you can reference.

---

## Clone Repo

Clone the repository and switch to the correct directory:

```bash
git clone https://github.com/mohamed-hashicorp/terraform_exercise.git
```

```bash
cd terraform_exercise/chapter5/loops-and-if-statements/live/global/existing-iam-user
```

---

## Identify an Existing IAM User

In your AWS account, choose any **existing** IAM username (e.g., visible in the AWS IAM console).

Open `main.tf` and set the username:

```hcl
resource "aws_iam_user" "existing_user" {
  name = "mohamed.ayman"
}
```

---

## Import the Existing IAM User

Initialize Terraform:

```bash
terraform init
```

Try applying the configuration:

```bash
terraform apply
```

You will get an error since the IAM user already exists — **this is expected**.

Now import the existing IAM user into Terraform state:

```bash
terraform import aws_iam_user.existing_user mohamed.ayman
```

Apply again:

```bash
terraform apply
```

Terraform will now recognize the IAM user and complete successfully.

---

## Delete Resources

After finishing the excersice, remove the resources by running the command:

```bash
terraform destroy
```


