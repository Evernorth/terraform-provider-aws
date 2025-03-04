---
subcategory: "SSO Admin"
layout: "aws"
page_title: "AWS: aws_ssoadmin_application_assignment"
description: |-
  Terraform resource for managing an AWS SSO Admin Application Assignment.
---

<!-- Please do not edit this file, it is generated. -->
# Resource: aws_ssoadmin_application_assignment

Terraform resource for managing an AWS SSO Admin Application Assignment.

## Example Usage

### Basic Usage

```typescript
// DO NOT EDIT. Code generated by 'cdktf convert' - Please report bugs at https://cdk.tf/bug
import { Construct } from "constructs";
import { Token, TerraformStack } from "cdktf";
/*
 * Provider bindings are generated by running `cdktf get`.
 * See https://cdk.tf/provider-generation for more details.
 */
import { SsoadminApplicationAssignment } from "./.gen/providers/aws/ssoadmin-application-assignment";
class MyConvertedCode extends TerraformStack {
  constructor(scope: Construct, name: string) {
    super(scope, name);
    new SsoadminApplicationAssignment(this, "example", {
      applicationArn: Token.asString(
        awsSsoadminApplicationExample.applicationArn
      ),
      principalId: Token.asString(awsIdentitystoreUserExample.userId),
      principalType: "USER",
    });
  }
}

```

### Group Type

```typescript
// DO NOT EDIT. Code generated by 'cdktf convert' - Please report bugs at https://cdk.tf/bug
import { Construct } from "constructs";
import { Token, TerraformStack } from "cdktf";
/*
 * Provider bindings are generated by running `cdktf get`.
 * See https://cdk.tf/provider-generation for more details.
 */
import { SsoadminApplicationAssignment } from "./.gen/providers/aws/ssoadmin-application-assignment";
class MyConvertedCode extends TerraformStack {
  constructor(scope: Construct, name: string) {
    super(scope, name);
    new SsoadminApplicationAssignment(this, "example", {
      applicationArn: Token.asString(
        awsSsoadminApplicationExample.applicationArn
      ),
      principalId: Token.asString(awsIdentitystoreGroupExample.groupId),
      principalType: "GROUP",
    });
  }
}

```

## Argument Reference

The following arguments are required:

* `applicationArn` - (Required) ARN of the application.
* `principalId` - (Required) An identifier for an object in IAM Identity Center, such as a user or group.
* `principalType` - (Required) Entity type for which the assignment will be created. Valid values are `USER` or `GROUP`.

## Attribute Reference

This resource exports the following attributes in addition to the arguments above:

* `id` - A comma-delimited string concatenating `applicationArn`, `principalId`, and `principalType`.

## Import

In Terraform v1.5.0 and later, use an [`import` block](https://developer.hashicorp.com/terraform/language/import) to import SSO Admin Application Assignment using the `id`. For example:

```typescript
// DO NOT EDIT. Code generated by 'cdktf convert' - Please report bugs at https://cdk.tf/bug
import { Construct } from "constructs";
import { TerraformStack } from "cdktf";
class MyConvertedCode extends TerraformStack {
  constructor(scope: Construct, name: string) {
    super(scope, name);
  }
}

```

Using `terraform import`, import SSO Admin Application Assignment using the `id`. For example:

```console
% terraform import aws_ssoadmin_application_assignment.example arn:aws:sso::012345678901:application/id-12345678,abcd1234,USER
```

<!-- cache-key: cdktf-0.20.0 input-da7337b5018a58007520a69e823fc2fc465c5c017370c5ce9dcee7d0009dcbc1 -->