# sumo-logic-forwarder

This template creates a Lambda function that sends log messages to Sumo Logic. It also includes a dead letter queue and a function that periodically retries sending of failed messages.

This template is a simplified version of the one found in the Sumo Logic repo:

https://github.com/SumoLogic/sumologic-aws-lambda/tree/master/cloudwatchlogs-with-dlq

It uses a YAML template and excludes email alerts, so you can use Datadog or another monitoring tool of choice instead.

## Deployment

Deployment is done via a single-file CloudFormation template. You can deploy this using the AWS console or the `aws cloudformation deploy` command.

### Parameters

* `CollectorURL` – The collector URL obtained from Sumo Logic.
