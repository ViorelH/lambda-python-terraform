# Serverless Python API with AWS Lambda + API Gateway + Terraform

This project demonstrates how to deploy a serverless Python API using AWS Lambda, API Gateway, and Terraform.

##  Project Overview

-  **AWS Lambda** — runs your Python function serverlessly.
-  **API Gateway** — exposes Lambda as an HTTP endpoint.
-  **Terraform** — automates the full infrastructure deployment.
-  **GitOps** — the entire configuration is stored in Git.

---

##  Project Structure

lambda-python-terraform/
├── lambda/
│ ├── main.py # Python function code
│ └── main.zip # Packaged Lambda code (ignored in Git)
├── main.tf # Main infrastructure config
├── provider.tf # AWS provider config
├── variables.tf # Terraform variables
├── outputs.tf # Outputs API Gateway URL
└── README.md # Documentation

---

##  Prerequisites

- AWS account + credentials configured (`aws configure`)
- Terraform installed (`terraform -v`)
- Python 3.x installed
- AWS CLI installed (`aws --version`)

---

##  Deployment Instructions

### 1️ Package Lambda Function

cd lambda
zip main.zip main.py
cd ..
### 2️ Initialize Terraform

terraform init
### 3️ Apply the Infrastructure

terraform apply
Confirm with yes.

### 4️ Get the API Endpoint
Terraform outputs your API Gateway URL:

Outputs:

api_endpoint = "https://xxxxxxxxxx.execute-api.us-east-1.amazonaws.com"
Test it by visiting the URL.

 Cleanup
To destroy all provisioned resources:

terraform destroy

 Security Considerations
This example uses public Lambda and API Gateway endpoints.

In production, you should consider:

Authentication (IAM or API keys)

Usage plans & throttling

Custom domains

Monitoring & logging with CloudWatch

🙌 Author
ViorelH — Project 8: Serverless Python API with Terraform & AWS
