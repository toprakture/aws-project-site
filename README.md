# AWS Static Website Deployment (CI/CD Enabled)

Automated static website hosting infrastructure on AWS, integrated with a continuous deployment pipeline powered by GitHub Actions.

---

## 📌 Architecture Overview

This project demonstrates an automated workflow for deploying static web assets to an Amazon S3 bucket configured for website hosting, fronted by an Application Load Balancer (ALB) for traffic management.

- **Storage & Hosting:** Amazon S3 (Static Website Hosting enabled)
- **Traffic Routing:** Application Load Balancer (ALB)
- **CI/CD Automation:** GitHub Actions
## 🚀 CI/CD Pipeline

The repository utilizes **GitHub Actions** for automated build and sync operations:

1. **Trigger:** Any `push` event targeting the `main` branch initiates the workflow.
2. **Authentication:** Uses AWS IAM credentials configured securely via repository secrets.
3. **Deployment:** Syncs updated static assets (HTML/CSS/JS) to the target S3 bucket using the AWS CLI.

---

## 🛠️ Configuration & Secrets

To replicate or deploy this project, configure the following **GitHub Actions Secrets** in your repository (`Settings > Secrets and variables > Actions`):

| Secret Name | Description |
| :--- | :--- |
| `AWS_ACCESS_KEY_ID` | IAM User Access Key with S3 Put/Sync permissions |
| `AWS_SECRET_ACCESS_KEY` | IAM User Secret Key |
| `AWS_REGION` | AWS Region where the bucket is hosted (e.g., `us-east-1`) |
| `S3_BUCKET_NAME` | Name of your target S3 bucket |

---

## 🔗 Architecture Endpoints *(Archived / Showcase)*

> **Note:** The cloud resources for this demonstration have been deprovisioned to prevent unnecessary AWS costs. Below are the architectural endpoint formats used during active deployment:

- **S3 Website Endpoint:** `http://<bucket-name>.s3-website-us-east-1.amazonaws.com`
- **Load Balancer Endpoint:** `http://<alb-name>-<id>.us-east-1.elb.amazonaws.com`


