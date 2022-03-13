# ExampleFargateRedis
Example AWS resources for Fargate + Elasticache Redis.

This cloudformation template will create:
* An ECS cluster that supports fargate and fargate spot.
* An ECR repo.
* A VPC, subnets, a (free!) internet gateway, an SSH ingress you can use for testing.
* A fargate task definition with a basic role, an example access policy, cloudwatch logging, and is tied to the ECR repo.
* An Elasticache Redis cluster. Note: deploying this template creates a running cluster that charges you.

## Prerequisites

### SAM CLI

This package assumes you have the SAM CLI installed on your developer instance. See: https://github.com/awsdocs/aws-sam-developer-guide/blob/master/doc_source/serverless-sam-cli-install-linux.md

## Usage

Build.

``` bash
# Resolve dependencies and create a .aws-sam/build/ directory.
$ sam build
```

Deploy to cloudformation. Use --guided for the initial install to setup your S3 bucket and what not.

``` bash
# Deploy the application. Use the guided method so you can fill in information about your S3 bucket and region.
$ sam deploy --guided
```