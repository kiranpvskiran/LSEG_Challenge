# LSEG_Challenge
LSEG Coding Challenge

Summary
Write a pseudo CI/CD pipeline one-click deployment code for hello world application. You can use any
tool/language of your choice. (Prefer Gitlab pipeline)

Bonus Points
• Secure way to use secrets
• Quality gate to pass/fail build on scan results
• Standard branch environment deployment control

# Hello World CI/CD Pipeline

This repository contains a simple "Hello World" application and a GitLab CI/CD pipeline for one-click deployment. The pipeline includes stages for building, testing, scanning, and deploying the application.

## Pipeline Overview

The GitLab CI/CD pipeline is defined in the `.gitlab-ci.yml` file and consists of the following stages:

1. **Build**: Builds the "Hello World" application.
2. **Test**: Runs a simple test to ensure the application is working correctly.
3. **Scan**: Performs a security scan to check for vulnerabilities.
4. **Deploy**: Deploys the application to different environments based on the branch name.

## Secure Secrets Management

Secrets are securely managed using GitLab CI/CD environment variables. The `SECRET_KEY` variable is an example of how secrets can be used in the pipeline.

## Quality Gate

The pipeline includes a quality gate in the `scan` stage. The build will pass or fail based on the results of the security scan.

## Branch-Based Deployment

The deployment stage uses branch-based environment control. The `main` branch is deployed to production, the `develop` branch is deployed to staging, and `feature/*` branches are deployed to feature-specific environments.
