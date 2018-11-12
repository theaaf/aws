# datadog-ecs

This template runs a Datadog agent container on each instance in an ECS cluster.

## Deployment

Deployment is done via a single-file CloudFormation template. You can deploy this using the AWS console or the `aws cloudformation deploy` command.

### Parameters

* `DatadogAPIKey` – This is your API key as provided by Datadog.
* `ECSCluster` – The name of the ECS cluster to run the agent in.
