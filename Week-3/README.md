# Week 3 of Cloud Computing Foundations

## Topics Covered
- Create an AWS Cloud Development Environment
- Create an Azure Cloud Development Environment
- Create a GCP Cloud Development Environment
- Applied Practice: Building a Multi-Cloud Continuous Integration Pipeline

## Create an AWS Cloud Development Environment
1. Create a Cloud9 service in the AWS portal and choose all the default settings
2. After deployment of the Cloud9, we can use the bash terminal to interact with other services in our aws cloud account.

    * Sample bash commands to list all the buckets in S3 or copy them
    ```bash
    aws s3 ls
    aws s3 cp
    ```
3. We can use the sidebars and create a lambda function 

![create-lambda](https://user-images.githubusercontent.com/92244042/179402103-6636b745-70e7-4061-bd9a-d677f98a04c2.png)

4. Create a GitHub repo and git clone into cloud9 environment via SSH to allow encrypted bidirectional communication

5. Create the [scaffold](https://github.com/jingyiyanlol/Coursera-Cloud-Computing-Foundations/blob/main/Week-3/scaffold) for the project

<div align='center'>
<img src="https://user-images.githubusercontent.com/92244042/179402446-976b2b1b-56f7-402b-81d4-fb28f5608cd8.png" width="60%">
</div>

6. Create GitHub Actions
    - Go to Actions > New workflow > set up a workflow yourself 
    - Configure the YAML file to run the workflow on a push trigger
    - Create Workflow Status Badge [![Run scaffold application test in week-3 folder with GitHub Actions](https://github.com/jingyiyanlol/Coursera-Cloud-Computing-Foundations/actions/workflows/week-3-aws-scaffold.yml/badge.svg)](https://github.com/jingyiyanlol/Coursera-Cloud-Computing-Foundations/actions/workflows/week-3-aws-scaffold.yml)


## Create an Azure Cloud Development Environment
1. Launch a cloud shell in Azure Portal

![launch cloud shell](https://user-images.githubusercontent.com/92244042/180607421-aa3a5503-3339-4e32-8128-b8b38dcf916c.png)

2. Create a virtual environment and clone this GitHub repository via SSH

4. Create a requirements-azure.txt that does not have the dependency "black" and update Makefile

4. Create GitHub Actions for Azure Python version 
[![Azure Run scaffold application test in week-3 folder](https://github.com/jingyiyanlol/Coursera-Cloud-Computing-Foundations/actions/workflows/scaffold-azure.yml/badge.svg)](https://github.com/jingyiyanlol/Coursera-Cloud-Computing-Foundations/actions/workflows/scaffold-azure.yml)

## Create a GCP Cloud Development Environment

1. Launch a cloud shell in GCP Console

![launch GCP cloud shell](https://user-images.githubusercontent.com/92244042/180649204-68d3e5f1-1f56-490a-a78d-00ed508cc923.png)

2. Git clone and cd into [gcp-flask-deploy](https://github.com/jingyiyanlol/Coursera-Cloud-Computing-Foundations/tree/main/Week-3/gcp-flask-deploy) directory.

3. Create and activate virtual environment

4. run `make install` to install dependencies

4. run below command to deploy the app

    ```basj
    gcloud app deploy
    ```
5. Set up push trigger for continuous delivery in gcp