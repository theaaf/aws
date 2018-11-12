# dns-name-target-nlb.cfn.yaml

This template creates a network load balancer that forwards HTTPS traffic to a given DNS name. At The Alliance, we use this to create private endpoint services for internal services that we need to make available to other VPCs or accounts.

You can read more about private endpoint services [here](https://docs.aws.amazon.com/vpc/latest/userguide/endpoint-service.html).

## Deployment

Deployment is done via a single-file CloudFormation template. You can deploy this using the AWS console or the `aws cloudformation deploy` command.

### Parameters

* `DNSName` – The DNS name to forward traffic to.
* `Subnets` – The subnets to place the network load balancer in.
* `VPC` – The VPN to place the network load balancer in.
