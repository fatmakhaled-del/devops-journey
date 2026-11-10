
# Terraform Docker Nginx

## Overview

This project demonstrates how to use Terraform to manage Docker infrastructure using Infrastructure as Code (IaC).

Terraform provisions an Nginx Docker image and container, maps it to a local port, and manages its lifecycle.

## Technologies

- Terraform v1.17.1
- Docker Desktop
- Docker Provider (kreuzwerker/docker)
- Nginx (Alpine)

## Project Structure

```text
terraform-docker-nginx/
├── main.tf
├── .gitignore
├── .terraform.lock.hcl
└── README.md
```

## Infrastructure

- Docker image: nginx:alpine
- Container name: terraform-nginx
- Container port: 80
- Local port: 8082

## Commands Used

Initialize Terraform:

```bash
terraform init
```

Preview infrastructure changes:

```bash
terraform plan
```

Create infrastructure:

```bash
terraform apply
```

List managed resources:

```bash
terraform state list
```

Destroy infrastructure:

```bash
terraform destroy
```

## What I Learned

- Infrastructure as Code fundamentals.
- Terraform providers and resources.
- Terraform initialization, planning, and applying.
- Terraform state management.
- Provisioning and destroying Docker containers using Terraform.
- Using `.gitignore` to protect local Terraform state files.

## Author

Fatma Khaled
