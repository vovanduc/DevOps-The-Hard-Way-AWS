# DevOps-The-Hard-Way-AWS

This tutorial contains a full, real-world solution for setting up an environment that is using DevOps technologies and practices for deploying apps and cloud services/cloud infrastructure to AWS.


The repository contains free labs, documentation, diagrams, and docs for setting up an entire workflow and DevOps environment from a real-world perspective in AWS.

## DevOps Scenario
The scenario that you're currently facing is you work in an organization that is very monolithic. There is a ton of bare metal, virtualization, manual deployments of applications, and **old school** practices based on the current teams knowledge of IT.

You're brought in to the company and team to make things more modern so the organization can not only succeed, but stay ahead of their competition. Management now understands the needs and complexity that comes with staying ahead of their competition and they know that they need to. Otherwise, the organization will fall...

## DevOps Solution
The solution is to deploy the Uber API for the sign-up page. Currently this solution is sitting on a bunch of baremetal, but it's time to sprinkle a little DevOps on it.

![](images/uber.png)

As a DevOps Engineer, you're more or less (most likely) not writing the app, but instead, deploying it. That's why you're not writing your own app in this tutorial.

*Full Disclosure* - I did have to edit this app a bit from Uber to make it compatible with Python3. You can find the repo here:

https://github.com/AdminTurnedDevOps/Python-Sample-Application

## Technology Details
You will be using the following technologies and platforms to set up a DevOps environment.

1. AWS
    - AWS will be used to host the application, cloud infrastructure, and any other services we may need to ensure the Uber app is deployed properly.
2. Python
    - Python will be used for the Uber app (it is written in Python) and some automation efforts that aren't in Terraform.
3. Terraform
   - Create an S3 bucket to store Terraform State files
   - Create an AWS ECR repository with Terraform
4. Docker
   - Create a Docker image
   - Store the Docker image in AWS ECR
5. Kubernetes
6. AWS CDK
7. CI/CD
8. Monitoring for applications and cloud services
9. GitHub
    - To store the application and infrastructure/automation code
10. Security best practices (DevSecOps)
    - Implement security best practices for the code you're writing and the cloud services you're building
11. Automated testing

## Labs
1. [Prerequisites](https://github.com/AdminTurnedDevOps/DevOps-The-Hard-Way-AWS/blob/main/prerequisites.md)
2. AWS:
    - [Configure credentials to access AWS at a programmatic level]()
2. Terraform - The purpose of the Terraform section is to create all of the AWS cloud services you'll need from an environment/infrastructure perspective to run the Uber application.
    - [Create S3 Bucket To Store TFSTATE Files](https://github.com/AdminTurnedDevOps/DevOps-The-Hard-Way-AWS/blob/main/Terraform-AWS-Services-Creation/1-Create-S3-Bucket-To-Store-TFSTATE-Files.md)
    - [Create an Elastic Container Registry](https://github.com/AdminTurnedDevOps/DevOps-The-Hard-Way-AWS/blob/main/Terraform-AWS-Services-Creation/2-Create-ECR.md)
3. Docker - The purpose of the Docker section is to create a Docker image from the app that the organization is running on-prem (the uber app), containerize it, and store the container inside of a container repository. For the container repo, you'll use AWS ECR.
    - [Create The Docker Image](https://github.com/AdminTurnedDevOps/DevOps-The-Hard-Way-AWS/blob/main/Docker/1-Create-Docker-Image.md)
    - [Log Into AWS ECR Repository](https://github.com/AdminTurnedDevOps/DevOps-The-Hard-Way-AWS/blob/main/Docker/Push%20Image%20To%20ECR.md)

## WIP
This project started on 5/16/2021 and is not done yet. I'm expecting the full thing to take 1-2 months based on my current time constraints.
