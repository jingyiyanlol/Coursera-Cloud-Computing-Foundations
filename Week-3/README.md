# Week 3 of Cloud Computing Foundations

## Topics Covered
- Create an AWS Cloud Development Environment
- Create an Azure Cloud Development Environment
- Create a GCP Cloud Development Environment
- Applied Practice: Building a Multi-Cloud Continuous Integration Pipeline


### Create an AWS Cloud Development Environment
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

[![Run scaffold application test in week-3 folder with GitHub Actions](https://github.com/jingyiyanlol/Coursera-Cloud-Computing-Foundations/actions/workflows/week-3-aws-scaffold.yml/badge.svg)](https://github.com/jingyiyanlol/Coursera-Cloud-Computing-Foundations/actions/workflows/week-3-aws-scaffold.yml)

![create-scaffold](https://user-images.githubusercontent.com/92244042/179402446-976b2b1b-56f7-402b-81d4-fb28f5608cd8.png)
