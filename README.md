# AWS Static Website Deployment (CI/CD Enabled)

This repository contains the static website files and GitHub Actions workflow for automatic deployment to S3.

## Website URLs
S3 Endpoint: http://aws-project-html-1.s3-website-us-east-1.amazonaws.com
Load Balancer URL: http:// lb-project1-852429630.us-east-1.elb.amazonaws.com 

## AWS Account ID
475241616261

## CI/CD Pipeline
- Push to `main` branch triggers automatic deployment.
- GitHub Actions uploads all static files to the S3 bucket.
