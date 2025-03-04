---
subcategory: "MemoryDB for Redis"
layout: "aws"
page_title: "AWS: aws_memorydb_subnet_group"
description: |-
  Provides information about a MemoryDB Subnet Group.
---


<!-- Please do not edit this file, it is generated. -->
# Resource: aws_memorydb_subnet_group

Provides information about a MemoryDB Subnet Group.

## Example Usage

```typescript
// DO NOT EDIT. Code generated by 'cdktf convert' - Please report bugs at https://cdk.tf/bug
import { Construct } from "constructs";
import { TerraformStack } from "cdktf";
/*
 * Provider bindings are generated by running `cdktf get`.
 * See https://cdk.tf/provider-generation for more details.
 */
import { DataAwsMemorydbSubnetGroup } from "./.gen/providers/aws/data-aws-memorydb-subnet-group";
class MyConvertedCode extends TerraformStack {
  constructor(scope: Construct, name: string) {
    super(scope, name);
    new DataAwsMemorydbSubnetGroup(this, "example", {
      name: "my-subnet-group",
    });
  }
}

```

## Argument Reference

The following arguments are required:

* `name` - (Required) Name of the subnet group.

## Attribute Reference

This data source exports the following attributes in addition to the arguments above:

* `id` - Name of the subnet group.
* `arn` - ARN of the subnet group.
* `description` - Description of the subnet group.
* `subnetIds` - Set of VPC Subnet ID-s of the subnet group.
* `vpcId` - VPC in which the subnet group exists.
* `tags` - Map of tags assigned to the subnet group.

<!-- cache-key: cdktf-0.20.0 input-a2199a4dfc692ac39b45aee765d1dc366111874bffd60dc24a73443b21e9d7d0 -->