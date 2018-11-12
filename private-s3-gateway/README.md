## private-s3-gateway

This template creates a private API gateway that makes an S3 bucket gettable to a single VPC. At The Alliance, we use this to host a private Sportradar API for internal use.

You can read more about private API gateways [here](https://docs.aws.amazon.com/apigateway/latest/developerguide/apigateway-private-apis.html).

## Deployment

Deployment is done via a single-file CloudFormation template. You can deploy this using the AWS console or the `aws cloudformation deploy` command.

### Parameters

* `S3Bucket` – The S3 bucket to make available.
* `Subnets` – The subnets to place the private VPC endpoint in. Generally, these should be private subnets, behind a NAT gateway.
* `VPC` – The VPN to place the private VPC endpoint in.
