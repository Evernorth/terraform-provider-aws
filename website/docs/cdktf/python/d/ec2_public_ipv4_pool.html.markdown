---
subcategory: "EC2 (Elastic Compute Cloud)"
layout: "aws"
page_title: "AWS: aws_ec2_public_ipv4_pool"
description: |-
  Provides details about a specific AWS EC2 Public IPv4 Pool.
---


<!-- Please do not edit this file, it is generated. -->
# Data Source: aws_ec2_public_ipv4_pool

Provides details about a specific AWS EC2 Public IPv4 Pool.

## Example Usage

### Basic Usage

```python
# DO NOT EDIT. Code generated by 'cdktf convert' - Please report bugs at https://cdk.tf/bug
from constructs import Construct
from cdktf import TerraformStack
#
# Provider bindings are generated by running `cdktf get`.
# See https://cdk.tf/provider-generation for more details.
#
from imports.aws.data_aws_ec2_public_ipv4_pool import DataAwsEc2PublicIpv4Pool
class MyConvertedCode(TerraformStack):
    def __init__(self, scope, name):
        super().__init__(scope, name)
        DataAwsEc2PublicIpv4Pool(self, "example",
            pool_id="ipv4pool-ec2-000df99cff0c1ec10"
        )
```

## Argument Reference

The following arguments are required:

* `pool_id` - (Required) AWS resource IDs of a public IPv4 pool (as a string) for which this data source will fetch detailed information.

## Attribute Reference

This data source exports the following attributes in addition to the arguments above:

* `description` - Description of the pool, if any.
* `network_border_group` - Name of the location from which the address pool is advertised.
* pool_address_ranges` - List of Address Ranges in the Pool; each address range record contains:
    * `address_count` - Number of addresses in the range.
    * `available_address_count` - Number of available addresses in the range.
    * `first_address` - First address in the range.
    * `last_address` - Last address in the range.
* `tags` - Any tags for the address pool.
* `total_address_count` - Total number of addresses in the pool.
* `total_available_address_count` - Total number of available addresses in the pool.

<!-- cache-key: cdktf-0.20.0 input-48bacd43b83d45d6042e5adf0821e82fae16e4191784bc09d4af47b05ff7cf8b -->