---
subcategory: "Managed Streaming for Kafka"
layout: "aws"
page_title: "AWS: aws_msk_configuration"
description: |-
  Get information on an Amazon MSK Configuration
---


<!-- Please do not edit this file, it is generated. -->
# Data Source: aws_msk_configuration

Get information on an Amazon MSK Configuration.

## Example Usage

```python
# DO NOT EDIT. Code generated by 'cdktf convert' - Please report bugs at https://cdk.tf/bug
from constructs import Construct
from cdktf import TerraformStack
#
# Provider bindings are generated by running `cdktf get`.
# See https://cdk.tf/provider-generation for more details.
#
from imports.aws.data_aws_msk_configuration import DataAwsMskConfiguration
class MyConvertedCode(TerraformStack):
    def __init__(self, scope, name):
        super().__init__(scope, name)
        DataAwsMskConfiguration(self, "example",
            name="example"
        )
```

## Argument Reference

This data source supports the following arguments:

* `name` - (Required) Name of the configuration.

## Attribute Reference

This data source exports the following attributes in addition to the arguments above:

* `arn` - ARN of the configuration.
* `latest_revision` - Latest revision of the configuration.
* `description` - Description of the configuration.
* `kafka_versions` - List of Apache Kafka versions which can use this configuration.
* `server_properties` - Contents of the server.properties file.

<!-- cache-key: cdktf-0.20.0 input-a4d86b249f9d4af6d96814d6f29e2a202f807b86ac9fffd8815b7aa4931e1636 -->