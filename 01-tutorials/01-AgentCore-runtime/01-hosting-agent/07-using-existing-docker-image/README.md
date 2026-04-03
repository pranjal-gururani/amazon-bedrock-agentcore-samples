# Hosting an Existing Docker Image in Amazon Bedrock AgentCore Runtime

## Overview

In this tutorial we will learn how to deploy an existing Docker image to Amazon Bedrock AgentCore Runtime, using the boto3 SDK directly.

We will focus on deploying a pre-built container image from Amazon ECR. 


### Tutorial Details

| Information         | Details                                                                                      |
|:--------------------|:---------------------------------------------------------------------------------------------|
| Tutorial type       | Conversational                                                                               |
| Agent type          | Single                                                                                       |
| Agentic Framework   | Strands Agents (pre-built in Docker image)                                                   |
| LLM model           | Anthropic Claude Haiku 4.5                                                                    |
| Tutorial components | Building Docker image, pushing to ECR, deploying to AgentCore Runtime using boto3            |
| Tutorial vertical   | Cross-vertical                                                                               |
| Example complexity  | Easy                                                                                         |
| SDK used            | boto3                                                                                        |

### Tutorial Architecture

In this tutorial we will describe how to build a Docker image containing a Strands Agent, push it to Amazon ECR, and deploy it to AgentCore Runtime using the `create_agent_runtime` API.

For demonstration purposes, we will  use the same Strands Agent from [01-strands-with-bedrock-model](../01-strands-with-bedrock-model) with two tools: `calculator` and `weather`.

### Tutorial Key Features

* Building and pushing Docker images for AgentCore Runtime
* Creating an IAM execution role for AgentCore Runtime
* Deploying to AgentCore Runtime using boto3
* Invoking and managing the deployed agent
