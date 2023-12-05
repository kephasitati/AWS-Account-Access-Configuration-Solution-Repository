# AWS Account Access Configuration Solution Repository

## Table of Contents

1. [Introduction](#introduction)
2. [Challenges](#challenges)
    - [Challenge #1: Application Developer Access Configuration](#challenge-1-application-developer-access-configuration)
        - [Task 1 (Sofía): Configuring an IAM Group and User](#task-1-sofía-configuring-an-iam-group-and-user)
        - [Task 2 (Nikhil): Logging in and Testing Access](#task-2-nikhil-logging-in-and-testing-access)
    - [Challenge #2: Database Administrator Access Configuration](#challenge-2-database-administrator-access-configuration)
        - [Task 3 (Sofía): Configuring IAM for Database Administrators](#task-3-sofía-configuring-iam-for-database-administrators)
        - [Task 4 (Olivia): Logging in and Resolving Issues](#task-4-olivia-logging-in-and-resolving-issues)
    - [Challenge #3: Refining IAM User Access](#challenge-3-refining-iam-user-access)
        - [Task 5 (Sofía): Custom IAM Policy and Simulator](#task-5-sofía-custom-iam-policy-and-simulator)
3. [How to Use This Repository](#how-to-use-this-repository)
4. [Disclaimer](#disclaimer)

## Introduction

Welcome to the GitHub repository for configuring AWS account access in a cafe's AWS environment. This repository provides detailed instructions and scripts for securing access for application developers and database administrators.

## Challenges

### Challenge #1: Application Developer Access Configuration

#### Task 1 (Sofía): Configuring an IAM Group and User

1. **IAM Group Creation:**
   - Create an IAM group named "AppDevelopers."
   - Attach policies: AmazonEC2ReadOnlyAccess, AWSCloud9EnvironmentMember.

2. **IAM User Configuration:**
   - Create an IAM user named "Nikhil" with AWS Management Console access.
   - Add Nikhil to the "AppDevelopers" group.

3. **AWS Cloud9 Environment Setup:**
   - Log in as Sofía (voclabs user).
   - Open AWS Cloud9 under DEVCafeServer.
   - Run commands for setting up the cafe web application.
   - Share AWS Cloud9 environment with Nikhil.

#### Task 2 (Nikhil): Logging in and Testing Access

1. **Incognito Mode Login:**
   - Log in as Nikhil using incognito mode.
   - Verify EC2 access, test the cafe web app, and check database connectivity.
   - Explore Systems Manager Parameter Store.

### Challenge #2: Database Administrator Access Configuration

#### Task 3 (Sofía): Configuring IAM for Database Administrators

1. **IAM Group Creation:**
   - Create an IAM group named "DBAdministrators."
   - Attach policies: AmazonRDSReadOnlyAccess, AmazonSSMFullAccess.

2. **IAM User Configuration:**
   - Create an IAM user named "Olivia" with AWS Management Console access.
   - Add Olivia to the "DBAdministrators" group.

#### Task 4 (Olivia): Logging in and Resolving Issues

1. **Incognito Mode Login:**
   - Log in as Olivia using incognito mode.
   - Verify RDS database status and address EC2 instance access issues.
   - Fix the database username issue in Systems Manager Parameter Store.

### Challenge #3: Refining IAM User Access

#### Task 5 (Sofía): Custom IAM Policy and Simulator

1. **IAM Policy Simulator:**
   - Use IAM Policy Simulator to evaluate permissions.
   - Select IAMReadOnlyAccess policy for Olivia.

2. **Custom IAM Policy Creation:**
   - Create a custom IAM policy to reduce allowed IAM actions for DBAdministrators.
   - Attach the custom policy and remove unnecessary IAMReadOnlyAccess.

## How to Use This Repository

1. Navigate to each challenge folder (Challenge_1, Challenge_2, Challenge_3).
2. Follow detailed instructions in the README files within each challenge folder.
3. Execute scripts and commands for AWS CLI or AWS Management Console operations.
4. Customize configurations based on your specific environment and security requirements.

## Disclaimer

This repository is intended for educational purposes. Before applying configurations in a production environment, review and adjust them according to your specific security and operational needs.
