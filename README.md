<!--lint disable double-link awesome-heading awesome-git-repo-age awesome-toc-->

<div align="center">
<p>
    <img
        style="width: 200px"
        width="200"
        src="https://avatars.githubusercontent.com/u/4426989?s=200&v=4"
    >
</p>
<h1>DevOps Reference</h1>

[Changelog](#) |
[Contributing](./CONTRIBUTING.md)

</div>
<div align="center">

[![Continious Integration][cibadge]][ciurl]
[![License: MIT][licensebadge]][licenseurl]

</div>

This repository contains different infrastructure components, CI/CD pipelines, automation tools
among other resources that are used in different projects here at [NaN Labs](https://www.nanlabs.com/).

## Contents

- [Apps and Boilerplates](#apps-and-boilerplates)
- [Examples](#examples)

  - [DevOps](#devops)
    - [A/B Testing](#ab-testing)
    - [Shell Scripting and CLI Tools](#shell-scripting-and-cli-tools)
    - [Continuous Integration, Delivery and Deployment](#continuous-integration-delivery-and-deployment)
    - [Containers, Orchestration and Serverless](#containers-orchestration-and-serverless)
      - [Containers and Compositions (Docker, Docker Compose, Buildpacks and more)](#containers-and-compositions-docker-docker-compose-buildpacks-and-more)
      - [DevContainers and Codespaces](#devcontainers-and-codespaces)
      - [Kubernetes](#kubernetes)
    - [Low Code solutions](#low-code-solutions)
      - [AWS Amplify](#aws-amplify)
    - [Infrastructure as Code](#infrastructure-as-code)
      - [Serverless Framework, SAM and CloudFormation](#serverless-framework-sam-and-cloudformation)
      - [Terraform](#terraform)
    - [Infrastructure from Code](#infrastructure-from-code)
      - [Klotho and more!](#klotho-and-more)
    - [ThirdParty Integrations](#thirdparty-integrations)
      - [Stripe](#stripe)

- [Contributing](#contributing)
- [Contributors](#contributors)

## Apps and Boilerplates

| Name                                                                                                                               | Description                                                                                                                                                                                                                                                                                                                                   | Keywords                                                                        |
| ---------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| [Basic AWS Glue ETL example app](https://github.com/nanlabs/devops-reference/tree/main/examples/serverless-glue-full-boilerplate/) | A complete example of an AWS Glue application that uses the [Serverless Framework](https://www.serverless.com/) to deploy the infrastructure and DevContainers and/or Docker Compose to run the application locally with AWS Glue Libs, Spark, Jupyter Notebook, AWS CLI, among other tools. It provides jobs using Python Shell and PySpark. | _Python_, _AWS_, _Glue_, _ETL_, _Serverless_, _DevContainers_, _Docker Compose_ |

## Examples

### DevOps

#### A/B Testing

| Name                                                                                                                 | Description                                                                                                  | Keywords                                                                               |
| -------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------- |
| [AWS CloudWatch Evidently](https://github.com/nanlabs/devops-reference/tree/main/examples/aws-cloudwatch-evidently/) | A complete analysis of the service and a Proof of Concept on how to integrate it with a Node.js application. | _Node.js_, _AWS_, _CloudWatch_, _CloudWatch Evidently_, _A/B Testing_, _Feature Flags_ |
| [Feature flags post](https://www.atlassian.com/continuous-delivery/principles/feature-flags)                         | How to progressively expose your features with feature flags by IAN BUCHANNAN.                               | _Feature Flags_                                                                        |

#### Shell Scripting and CLI Tools

| Name                                                                                                                                                       | Description                                                                 | Keywords                                       |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------- | ---------------------------------------------- |
| [Bash as a Wrapper Utility](https://github.com/nanlabs/devops-reference/tree/main/examples/bash-as-a-wrapper-utility-basic/)                               | Bash as a wrapper utility for other languages and tools.                    | _Shell Scripting_, _Utilities_                 |
| [Bash as a Wrapper Utility with Easy Options](https://github.com/nanlabs/devops-reference/tree/main/examples/bash-as-a-wrapper-utility-with-easy-options/) | Bash as a wrapper utility for other languages and tools using Easy Options. | _Shell Scripting_, _Utilities_, _Easy Options_ |
| [Easy Options](https://github.com/nanlabs/devops-reference/tree/main/examples/easy-options/)                                                               | Easy options for shell scripts.                                             | _Shell Scripting_, _Utilities_, _Easy Options_ |
| [When to use shell](https://google.github.io/styleguide/shellguide.html#when-to-use-shell)                                                                 | A guide from Google on when to use shell scripts.                           | _Shell Scripting_, _Utilities_                 |

#### Continuous Integration, Delivery and Deployment

| Name                                                                                                                                                            | Description                                                                                                                                                                                                                                                                                                                        | Keywords                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| [Actionlint Playground](https://rhysd.github.io/actionlint/)                                                                                                    | Static checker for GitHub Actions workflow files.                                                                                                                                                                                                                                                                                  | _GitHub Actions_, _Actionlint_                                         |
| [Automate Pull Requests Reviews using Danger](https://github.com/nanlabs/devops-reference/tree/main/.github/workflows/pr-review.yml)                            | This workflow automates the initial review of Pull Requests using [Danger.js](https://danger.systems/js/). This provides another logical step in your build, through this Danger can help lint your rote tasks in daily code review. You can use Danger to codify your teams norms. Leaving humans to think about harder problems. | _GitHub Actions_, _Danger.js_                                          |
| [Automating Pull Request Review using DangerJS and GitHub Actions](https://github.com/nanlabs/devops-reference/tree/main/examples/github-actions-with-dangerjs) | Learn how to automate Pull Request (PR) reviews using DangerJS and GitHub Actions. Automating PR reviews helps enforce coding standards, catch potential issues, and improve code quality in your GitHub repository.                                                                                                               | _Tutorial_, _GitHub Actions_, _DangerJS_, _Pull Request_, _Automation_ |
| [Automation Seed example](https://github.com/nanlabs/automation-seed/tree/main/.github/workflows)                                                               | Different workflows to validate the code and deploy an automation report page.                                                                                                                                                                                                                                                     | _GitHub Actions_, _Automation_                                         |
| [Markdown Lint](https://github.com/nanlabs/devops-reference/tree/main/.github/workflows/markdownlint.yml)                                                       | This workflow validates the Markdown files in the repository using the [markdownlint action](https://github.com/marketplace/actions/markdown-lint).                                                                                                                                                                                | _GitHub Actions_, _Markdown Lint_                                      |
| [React Boilerplate](https://github.com/nanlabs/react-boilerplate/tree/main/.github/workflows)                                                                   | Different workflows to validate the code and deploy a React application.                                                                                                                                                                                                                                                           | _GitHub Actions_, _React_                                              |
| [Shell Check](https://github.com/nanlabs/devops-reference/tree/main/.github/workflows/shellcheck.yml)                                                           | This workflow validates the shell scripts in the repository using the [shellcheck action](https://github.com/ludeeus/action-shellcheck).                                                                                                                                                                                           | _GitHub Actions_, _Shell Check_                                        |
| [Terraform Check](https://github.com/nanlabs/devops-reference/tree/main/.github/workflows/tf-check.yml)                                                         | This workflow validates the Terraform files in the repository using the [terraform action](https://github.com/dflook/terraform-fmt-check).                                                                                                                                                                                         | _GitHub Actions_, _Terraform_                                          |
| [TODOs to GitHub Issues](https://github.com/nanlabs/devops-reference/tree/main/examples/github-actions-todo-to-issue/)                                          | This tutorial shows how to create a GitHub Action that converts TODO comments into GitHub issues.                                                                                                                                                                                                                                  | _GitHub Actions_, _TODOs_, _Issues_                                    |

#### Containers, Orchestration and Serverless

##### Containers and Compositions (Docker, Docker Compose, Buildpacks and more)

| Name                                                                                                                                             | Description                                                                                                                                                                                                                             | Keywords                                                                       |
| ------------------------------------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------ |
| [Airflow and Spark environment using Docker and Docker Compose](https://github.com/nanlabs/devops-reference/tree/main/examples/compose-airflow/) | Dockerfile and compose.yml to run Airflow locally with initialization scripts.                                                                                                                                                          | _Docker_, _Docker Compose_, _Airflow_, _Spark_                                 |
| [AWS Cognito local using Docker Compose](https://github.com/nanlabs/devops-reference/tree/main/examples/compose-cognito/)                        | compose.yml to run Cognito locally.                                                                                                                                                                                                     | _Docker_, _Docker Compose_, _Cognito_, _AWS_                                   |
| [AWS Glue using Docker and Docker Compose](https://github.com/nanlabs/devops-reference/tree/main/examples/compose-glue/)                         | Dockerfile and compose.yml for AWS Glue development with AWS Glue Libs, Spark, Jupyter Notebook, AWS CLI among other tools.                                                                                                             | _Docker_, _Docker Compose_, _AWS Glue_, _Spark_, _Jupyter Notebook_, _AWS CLI_ |
| [AWS Neptune using Docker and Docker Compose](https://github.com/nanlabs/devops-reference/tree/main/examples/compose-neptune/)                   | Dockerfile and compose.yml to run AWS Neptune locally with initialization scripts.                                                                                                                                                      | _Docker_, _Docker Compose_, _AWS Neptune_                                      |
| [Docker Compose NestJS Starter App](https://github.com/nanlabs/devops-reference/tree/main/examples/compose-nestjs)                               | Docker Compose starter app for NestJS.                                                                                                                                                                                                  | _Docker_, _Docker Compose_, _NestJS_, _Node.js_                                |
| [Localstack using Docker and Docker Compose](https://github.com/nanlabs/devops-reference/tree/main/examples/compose-localstack/)                 | Dockerfile and compose.yml to run Localstack locally with all the necessary services. This example also includes a script to create the necessary resources in Localstack. The provided examples are for DynamoDB, S3, SQS and Kinesis. | _Docker_, _Docker Compose_, _Localstack_, _DynamoDB_, _S3_, _SQS_, _Kinesis_   |
| [Microsoft SQL Server using Docker and Docker Compose](https://github.com/nanlabs/devops-reference/tree/main/examples/compose-mssql/)            | Dockerfile and compose.yml to run Microsoft SQL Server locally with initialization scripts.                                                                                                                                             | _Docker_, _Docker Compose_, _Microsoft SQL Server_                             |
| [MongoDB + Mongo Express using Docker and Docker Compose](https://github.com/nanlabs/devops-reference/tree/main/examples/compose-mongodb/)       | Dockerfile and compose.yml to run MongoDB and Mongo Express locally with initialization scripts.                                                                                                                                        | _Docker_, _Docker Compose_, _MongoDB_, _Mongo Express_                         |
| [PostgreSQL using Docker and Docker Compose](https://github.com/nanlabs/devops-reference/tree/main/examples/compose-postgres/)                   | Dockerfile and compose.yml to run PostgreSQL locally with initialization scripts.                                                                                                                                                       | _Docker_, _Docker Compose_, _PostgreSQL_                                       |
| [Python Buildpack](https://github.com/nanlabs/devops-reference/tree/main/examples/buildpacks-python)                                             | Buildpack example for Python applications.                                                                                                                                                                                              | _Buildpack_, _Python_                                                          |

##### DevContainers and Codespaces

| Name                                                                                           | Description                                                                                                                                                                                                                         | Keywords                                                                                                                                   |
| ---------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| [AWS Glue](https://github.com/nanlabs/devops-reference/tree/main/examples/devcontainers-glue/) | DevContainer for AWS Glue development. Uses `docker-compose` to run VSCode attached to a container with all the necessary tools to develop AWS Glue jobs such us AWS Glue Libs, Spark, Jupyter Notebook, AWS CLI among other tools. | _Docker_, _Docker Compose_, _DevContainer_, _VSCode DevContainer_, _GitHub Codespaces_, _AWS Glue_, _Spark_, _Jupyter Notebook_, _AWS CLI_ |

##### Kubernetes

| Name                                                                                                  | Description                                                                                                                                  | Keywords                                            |
| ----------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------- |
| [Ingress](https://github.com/nanlabs/devops-reference/tree/main/examples/kubernetes-ingress-example/) | Ingress example using NGINX Ingress Controller. You can run this example locally using [Minikube](https://minikube.sigs.k8s.io/docs/start/). | _Kubernetes_, _Ingress_, _NGINX Ingress Controller_ |

#### Low Code solutions

##### AWS Amplify

| Name                                                                                                                 | Description                                                          | Keywords                             |
| -------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------- | ------------------------------------ |
| [AWS Amplify + NextJS 13](https://github.com/nanlabs/devops-reference/tree/main/examples/amplify-nextjs-deployment/) | AWS Amplify example to deploy a NextJS v13 application to the Cloud. | _AWS Amplify_, _NextJS_, _NextJS 13_ |

#### Infrastructure as Code

##### Serverless Framework, SAM and CloudFormation

| Name                                                                                                                                                                             | Description                                                                                                                                                                                                                                                                                                          | Keywords                                                                                              |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- |
| [AWS AppSync + Python](https://github.com/nanlabs/devops-reference/tree/main/examples/serverless-appsync-python/)                                                                | Serverless Framework example to deploy an AWS AppSync API using Python. It also has a local development environment using [Serverless Offline](https://www.serverless.com/plugins/serverless-offline).                                                                                                               | _Serverless Framework_, _AWS AppSync_, _Python_                                                       |
| [AWS AppSync + TypeScript](https://github.com/nanlabs/devops-reference/tree/main/examples/serverless-appsync-node-typescript/)                                                   | Serverless Framework example to deploy an AWS AppSync API using TypeScript. It also has a local development environment using [Serverless Offline](https://www.serverless.com/plugins/serverless-offline).                                                                                                           | _Serverless Framework_, _AWS AppSync_, _TypeScript_                                                   |
| [AWS Cognito Local Example](https://github.com/nanlabs/devops-reference/tree/main/examples/serverless-cognito-local/)                                                            | AWS Cognito local enviroment with Docker and Serverless offline                                                                                                                                                                                                                                                      | _Serverless Framework_, _Serverless Offline_, _AWS_, _Cognito_, _Docker_                              |
| [AWS Glue with Python Shell and PySpark Jobs](https://github.com/nanlabs/devops-reference/tree/main/examples/serverless-glue-deployment/)                                        | Serverless Framework example to deploy an AWS Glue job using Python Shell and PySpark.                                                                                                                                                                                                                               | _Serverless Framework_, _AWS Glue_, _Python Shell_, _PySpark_                                         |
| [DocumentDB Cluster](https://github.com/nanlabs/devops-reference/tree/main/examples/serverless-documentdb/)                                                                      | Serverless Framework example to deploy a DocumentDB cluster with all the necessary resources.                                                                                                                                                                                                                        | _Serverless Framework_, _DocumentDB_                                                                  |
| [Neo4j in EC2](https://github.com/nanlabs/devops-reference/tree/main/examples/serverless-neo4j-ec2/)                                                                             | Serverless Framework example to deploy a Neo4j instance in EC2.                                                                                                                                                                                                                                                      | _Serverless Framework_, _Neo4j_, _EC2_                                                                |
| [RDS Postgres Instance](https://github.com/nanlabs/devops-reference/tree/main/examples/serverless-rds-postgres/)                                                                 | Serverless Framework example to deploy a RDS Postgres instance with all the necessary resources.                                                                                                                                                                                                                     | _Serverless Framework_, _RDS Postgres_                                                                |
| [RDS Postgres Instance with Serverless VPC Plugin](https://github.com/nanlabs/devops-reference/tree/main/examples/serverless-rds-postgres-vpc-plugin/)                           | Serverless Framework example to deploy a RDS Postgres instance with all the necessary resources using [Serverless VPC Plugin](https://www.serverless.com/plugins/serverless-vpc-plugin).                                                                                                                             | _Serverless Framework_, _RDS Postgres_, _Serverless VPC Plugin_                                       |
| [Serverless + FastAPI](https://github.com/nanlabs/devops-reference/tree/main/examples/serverless-python-fastapi/)                                                                | Serverless Framework example to deploy a FastAPI application using Python. It also has local development environment using [Serverless Offline](https://www.serverless.com/plugins/serverless-offline).                                                                                                              | _Serverless Framework_, _Serverless Offline_, _FastAPI_, _Python_                                     |
| [Serverless Middy](https://github.com/nanlabs/devops-reference/tree/main/examples/serverless-node-typescript-middy/)                                                             | Serverless Framework example to deploy a lambda function using [Middy](https://middy.js.org/), the stylish Node.js middleware engine for AWS Lambda.                                                                                                                                                                 | _Serverless Framework_, _Middy_                                                                       |
| [Serverless Middy with Custom Middleware](https://github.com/nanlabs/devops-reference/tree/main/examples/serverless-node-typescript-middy-custom-middleware/)                    | Serverless Framework example to deploy a lambda function using [Middy](https://middy.js.org/), the stylish Node.js middleware engine for AWS Lambda.                                                                                                                                                                 | _Serverless Framework_, _Middy_, _Custom Middleware_                                                  |
| [Serverless Nest Application with TypeScript](https://github.com/nanlabs/devops-reference/tree/main/examples/serverless-node-typescript-nest/)                                   | Serverless Framework example to deploy a NestJS application using TypeScript.                                                                                                                                                                                                                                        | _Serverless Framework_, _NestJS_, _TypeScript_                                                        |
| [Serverless S3 Local](https://github.com/nanlabs/devops-reference/tree/main/examples/serverless-s3-local/)                                                                       | Serverless Framework example to run a lambda function locally using [Serverless S3 Local](https://www.serverless.com/plugins/serverless-s3-local).                                                                                                                                                                   | _Serverless Framework_, _Serverless S3 Local_                                                         |
| [Serverless SQS offline + Python + Localstack Example](https://github.com/nanlabs/devops-reference/tree/main/examples/serverless-sqs-python/)                                    | Serverless Framework example to run lambda functions locally using [Serverless Offline SQS](https://www.serverless.com/plugins/serverless-offline-sqs-external) with Localstack. It provides a full local development environment using [Serverless Offline](https://www.serverless.com/plugins/serverless-offline). | _Serverless Framework_, _SQS_, _Serverless Offline_, _Serverless Offline SQS_, _Localstack_, _Python_ |
| [Serverless SQS offline + TypeScript + ElasticMQ Example](https://github.com/nanlabs/devops-reference/tree/main/examples/serverless-sqs-node-typescript-offline-with-elasticmq/) | Serverless Framework example to run lambda functions locally using [Serverless Offline SQS](https://www.serverless.com/plugins/serverless-offline-sqs) with ElasticMQ. It provides a full local development environment using [Serverless Offline](https://www.serverless.com/plugins/serverless-offline).           | _Serverless Framework_, _SQS_, _Serverless Offline_, _Serverless Offline SQS_, _ElasticMQ_            |
| [Serverless Twilio + Typescript Lambda example](https://github.com/nanlabs/devops-reference/tree/main/examples/serverless-twilio-aws-lambdas-typescript/)                        | Serverless Framework example to deploy a lambda function using Twilio and TypeScript.                                                                                                                                                                                                                                | _Serverless Framework_, _Serverless Offline_, _AWS_, _Twilio_, _TypeScript_                           |
| [Start and Stop EC2 Instances with AWS Lambda](https://github.com/nanlabs/devops-reference/tree/main/examples/serverless-start-stop-ec2-instance/)                               | Serverless Framework example to start and stop EC2 instances using AWS Lambda.                                                                                                                                                                                                                                       | _Serverless Framework_, _EC2_, _AWS Lambda_                                                           |
| [Using Serverless Framework with Terraform](https://github.com/nanlabs/devops-reference/tree/main/examples/serverless-terraform-example)                                         | The definitive example of how to use Terraform and Serverless Framework together.                                                                                                                                                                                                                                    | _Serverless Framework_, _Terraform_, _AWS_                                                            |

##### Terraform

| Name                                                                                                                                                                           | Description                                                                                                                  | Keywords                                         |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------ |
| [Terraform AWS Minecraft Server](https://github.com/nanlabs/devops-reference/tree/main/examples/terraform-aws-minecraft-server/)                                               | Terraform example to deploy a Minecraft server in AWS EC2 instance using Docker.                                             | _Terraform_, _AWS_, _Minecraft_, _Docker_, _EC2_ |
| [Terraform AWS RDS Postgres instance](https://github.com/nanlabs/devops-reference/tree/main/examples/terraform-vpc-rds-instance-bastion-starter/modules/rds)                   | Terraform module for creating AWS RDS Postgres instance.                                                                     | _Terraform_, _AWS_, _RDS_                        |
| [Terraform AWS VPC resources](https://github.com/nanlabs/devops-reference/tree/main/examples/terraform-vpc-rds-instance-bastion-starter/modules/vpc)                           | Terraform module for creating AWS VPC resources.                                                                             | _Terraform_, _AWS_, _VPC_                        |
| [Terraform Bastion Host](https://github.com/nanlabs/devops-reference/tree/main/examples/terraform-vpc-rds-instance-bastion-starter/modules/bastion)                            | Terraform module which creates an EC2 instance acting as a bastion host                                                      | _Terraform_, _AWS_, _Bastion_                    |
| [Terraform Starter Kit for AWS VPC, RDS instance, and Bastion Host](https://github.com/nanlabs/devops-reference/tree/main/examples/terraform-vpc-rds-instance-bastion-starter) | Terraform Starter kit for creating AWS infrastructure using Terraform that contains a VPC, RDS instance, and a bastion host. | _Terraform_, _AWS_, _VPC_, _RDS_, _Bastion_      |
| [Using Serverless Framework with Terraform](https://github.com/nanlabs/devops-reference/tree/main/examples/serverless-terraform-example)                                       | The definitive example of how to use Terraform and Serverless Framework together.                                            | _Serverless Framework_, _Terraform_, _AWS_       |

#### Infrastructure from Code

##### Klotho and more

| Name                                                                                      | Description                                                                                             | Keywords                                |
| ----------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | --------------------------------------- |
| [Klotho](https://github.com/nanlabs/devops-reference/tree/main/examples/klotho-analysis/) | A complete analysis of the service and a Proof of Concept on how to integrate it with a GO application. | _AWS_, _Pulumi_, _Deployment_, _Klotho_ |

#### ThirdParty Integrations

##### Stripe

| Name                                                                                                                                                   | Description                                                                                                                                                                                                                                                                                    | Keywords                                                                               |
| ------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| [Stripe Integration with Node.js and TypeScript](https://github.com/nanlabs/devops-reference/tree/main/examples/stripe-integration-nodejs-typescript/) | This project offers a seamless Stripe integration with Node.js and TypeScript, providing a powerful API for managing basic operations like customer creation, checkout sessions, and portal sessions. It empowers developers to effortlessly handle payment-related tasks with the Stripe API. | _Node.js_, _TypeScript_, _Stripe_, _Payment Gateway_, _API_, _Integration_, _Webhooks_ |

## Contributing

- Contributions make the open source community such an amazing place to learn, inspire, and create.
- Any contributions you make are **truly appreciated**.
- Check out our [contribution guidelines](./CONTRIBUTING.md) for more information.

## Contributors

<a href="https://github.com/nanlabs/devops-reference/contributors">
  <img src="https://contrib.rocks/image?repo=nanlabs/devops-reference"/>
</a>

Made with [contributors-img](https://contrib.rocks).

[cibadge]: https://github.com/nanlabs/devops-reference/actions/workflows/ci.yml/badge.svg
[licensebadge]: https://img.shields.io/badge/License-MIT-blue.svg
[ciurl]: https://github.com/nanlabs/devops-reference/actions/workflows/ci.yml
[licenseurl]: https://github.com/nanlabs/devops-reference/blob/main/LICENSE
