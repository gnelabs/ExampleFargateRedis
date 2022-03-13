# ExampleFargateRedis
Example AWS resources for Fargate + Elasticache Redis.

## Prerequisites

### SAM CLI

This package assumes you have the SAM CLI installed on your developer instance. See: https://github.com/awsdocs/aws-sam-developer-guide/blob/master/doc_source/serverless-sam-cli-install-linux.md

### Docker (For testing and development)

If you want to test and develop, you're going to want docker to be installed so you can run the local lambda docker container. This will allow you to run sam local commands. See: https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/serverless-sam-cli-install-linux.html#serverless-sam-cli-install-linux-docker

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