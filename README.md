# terraform_project1

# AWS Infrastructure Automation with Terraform

This project demonstrates the use of **Terraform (Infrastructure as Code)** to automate the provisioning of a secure, scalable, and highly available environment on **AWS**.

## 🏗️ Architecture Overview
The Terraform configuration automates the deployment of:
- **Custom VPC:** Including Public and Private Subnets across multiple Availability Zones.
- **Compute:** EC2 instances with specific Security Groups and IAM Roles.
- **Networking:** Internet Gateway, Route Tables, and NAT Gateway for private subnet connectivity.
- **Storage:** S3 Buckets for state management or static asset hosting.
- **Load Balancing:** (Optional) Application Load Balancer to distribute incoming traffic.

## 🚀 Purpose & Learning Objectives
As an aspiring **Cloud Support Engineer**, I built this project to master:
- **Infrastructure as Code (IaC):** Reducing manual configuration errors through automation.
- **State Management:** Understanding `terraform.tfstate` and remote backends.
- **Modular Design:** Writing reusable Terraform modules for VPC and EC2.
- **Troubleshooting:** Identifying and resolving provider errors and resource dependency issues.

## 🛠️ Prerequisites
- [Terraform](https://www.terraform.io/downloads.html) installed (v1.0+)
- AWS CLI configured with appropriate IAM permissions.
- An S3 bucket (if using a remote backend for state files).

## 🔧 Deployment Steps

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/taufique003/terraform_project1.git](https://github.com/taufique003/terraform_project1.git)
   cd terraform_project1

**   Initialize Terraform:** Downloads providers and initializes the backend.
Bash
terraform init

**Plan the Deployment:** Review the resources that will be created.
Bash
terraform plan

**Apply Changes:** Provision the infrastructure on AWS.
Bash
terraform apply -auto-approve

**Cleanup:** Destroy all resources to avoid unnecessary AWS costs.
Bash
terraform destroy

**📂 File Structure**
main.tf: Primary configuration for resource definitions.

variables.tf: Input variables for customization (Regions, Instance types).

outputs.tf: Key information displayed after deployment (Instance IPs, DNS names).

provider.tf: AWS provider and version configuration.
