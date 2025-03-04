---
subcategory: "Network Manager"
layout: "aws"
page_title: "AWS: aws_networkmanager_connection"
description: |-
  Creates a connection between two devices.
---


<!-- Please do not edit this file, it is generated. -->
# Resource: aws_networkmanager_connection

Creates a connection between two devices.
The devices can be a physical or virtual appliance that connects to a third-party appliance in a VPC, or a physical appliance that connects to another physical appliance in an on-premises network.

## Example Usage

```python
# DO NOT EDIT. Code generated by 'cdktf convert' - Please report bugs at https://cdk.tf/bug
from constructs import Construct
from cdktf import Token, TerraformStack
#
# Provider bindings are generated by running `cdktf get`.
# See https://cdk.tf/provider-generation for more details.
#
from imports.aws.networkmanager_connection import NetworkmanagerConnection
class MyConvertedCode(TerraformStack):
    def __init__(self, scope, name):
        super().__init__(scope, name)
        NetworkmanagerConnection(self, "example",
            connected_device_id=example2.id,
            device_id=example1.id,
            global_network_id=Token.as_string(aws_networkmanager_global_network_example.id)
        )
```

## Argument Reference

This resource supports the following arguments:

* `connected_device_id` - (Required) The ID of the second device in the connection.
* `connected_link_id` - (Optional) The ID of the link for the second device.
* `description` - (Optional) A description of the connection.
* `device_id` - (Required) The ID of the first device in the connection.
* `global_network_id` - (Required) The ID of the global network.
* `link_id` - (Optional) The ID of the link for the first device.
* `tags` - (Optional) Key-value tags for the connection. If configured with a provider [`default_tags` configuration block](https://registry.terraform.io/providers/hashicorp/aws/latest/docs#default_tags-configuration-block) present, tags with matching keys will overwrite those defined at the provider-level.

## Attribute Reference

This resource exports the following attributes in addition to the arguments above:

* `arn` - The Amazon Resource Name (ARN) of the connection.
* `tags_all` - A map of tags assigned to the resource, including those inherited from the provider [`default_tags` configuration block](https://registry.terraform.io/providers/hashicorp/aws/latest/docs#default_tags-configuration-block).

## Import

In Terraform v1.5.0 and later, use an [`import` block](https://developer.hashicorp.com/terraform/language/import) to import `aws_networkmanager_connection` using the connection ARN. For example:

```python
# DO NOT EDIT. Code generated by 'cdktf convert' - Please report bugs at https://cdk.tf/bug
from constructs import Construct
from cdktf import TerraformStack
class MyConvertedCode(TerraformStack):
    def __init__(self, scope, name):
        super().__init__(scope, name)
```

Using `terraform import`, import `aws_networkmanager_connection` using the connection ARN. For example:

```console
% terraform import aws_networkmanager_connection.example arn:aws:networkmanager::123456789012:device/global-network-0d47f6t230mz46dy4/connection-07f6fd08867abc123
```

<!-- cache-key: cdktf-0.20.0 input-950e6f1e6e30f9c05d70308c91abfbf81e3cb619be3e1bdef3b486654d0ee394 -->