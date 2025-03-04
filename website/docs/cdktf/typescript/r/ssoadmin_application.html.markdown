---
subcategory: "SSO Admin"
layout: "aws"
page_title: "AWS: aws_ssoadmin_application"
description: |-
  Terraform resource for managing an AWS SSO Admin Application.
---

<!-- Please do not edit this file, it is generated. -->
# Resource: aws_ssoadmin_application

Terraform resource for managing an AWS SSO Admin Application.

## Example Usage

### Basic Usage

```typescript
// DO NOT EDIT. Code generated by 'cdktf convert' - Please report bugs at https://cdk.tf/bug
import { Construct } from "constructs";
import { Fn, Token, TerraformStack } from "cdktf";
/*
 * Provider bindings are generated by running `cdktf get`.
 * See https://cdk.tf/provider-generation for more details.
 */
import { DataAwsSsoadminInstances } from "./.gen/providers/aws/data-aws-ssoadmin-instances";
import { SsoadminApplication } from "./.gen/providers/aws/ssoadmin-application";
class MyConvertedCode extends TerraformStack {
  constructor(scope: Construct, name: string) {
    super(scope, name);
    const example = new DataAwsSsoadminInstances(this, "example", {});
    const awsSsoadminApplicationExample = new SsoadminApplication(
      this,
      "example_1",
      {
        applicationProviderArn: "arn:aws:sso::aws:applicationProvider/custom",
        instanceArn: Token.asString(
          Fn.lookupNested(Fn.tolist(example.arns), ["0"])
        ),
        name: "example",
      }
    );
    /*This allows the Terraform resource name to match the original name. You can remove the call if you don't need them to match.*/
    awsSsoadminApplicationExample.overrideLogicalId("example");
  }
}

```

### With Portal Options

```typescript
// DO NOT EDIT. Code generated by 'cdktf convert' - Please report bugs at https://cdk.tf/bug
import { Construct } from "constructs";
import { Fn, Token, TerraformStack } from "cdktf";
/*
 * Provider bindings are generated by running `cdktf get`.
 * See https://cdk.tf/provider-generation for more details.
 */
import { DataAwsSsoadminInstances } from "./.gen/providers/aws/data-aws-ssoadmin-instances";
import { SsoadminApplication } from "./.gen/providers/aws/ssoadmin-application";
class MyConvertedCode extends TerraformStack {
  constructor(scope: Construct, name: string) {
    super(scope, name);
    const example = new DataAwsSsoadminInstances(this, "example", {});
    const awsSsoadminApplicationExample = new SsoadminApplication(
      this,
      "example_1",
      {
        applicationProviderArn: "arn:aws:sso::aws:applicationProvider/custom",
        instanceArn: Token.asString(
          Fn.lookupNested(Fn.tolist(example.arns), ["0"])
        ),
        name: "example",
        portalOptions: [
          {
            signInOptions: [
              {
                applicationUrl: "http://example.com",
                origin: "APPLICATION",
              },
            ],
            visibility: "ENABLED",
          },
        ],
      }
    );
    /*This allows the Terraform resource name to match the original name. You can remove the call if you don't need them to match.*/
    awsSsoadminApplicationExample.overrideLogicalId("example");
  }
}

```

## Argument Reference

The following arguments are required:

* `applicationProviderArn` - (Required) ARN of the application provider.
* `instanceArn` - (Required) ARN of the instance of IAM Identity Center.
* `name` - (Required) Name of the application.

The following arguments are optional:

* `clientToken` - (Optional) A unique, case-sensitive ID that you provide to ensure the idempotency of the request. AWS generates a random value when not provided.
* `description` - (Optional) Description of the application.
* `portalOptions` - (Optional) Options for the portal associated with an application. See [`portalOptions`](#portal_options-argument-reference) below.
* `status` - (Optional) Status of the application. Valid values are `ENABLED` and `DISABLED`.
* `tags` - (Optional) Key-value mapping of resource tags. If configured with a provider [`defaultTags` configuration block](/docs/providers/aws/index.html#default_tags-configuration-block) present, tags with matching keys will overwrite those defined at the provider-level.

### `portalOptions` Argument Reference

* `signInOptions` - (Optional) Sign-in options for the access portal. See [`signInOptions`](#sign_in_options-argument-reference) below.
* `visibility` - (Optional) Indicates whether this application is visible in the access portal. Valid values are `ENABLED` and `DISABLED`.

### `signInOptions` Argument Reference

* `applicationUrl` - (Optional) URL that accepts authentication requests for an application.
* `origin` - (Required) Determines how IAM Identity Center navigates the user to the target application.
Valid values are `APPLICATION` and `IDENTITY_CENTER`.
If `APPLICATION` is set, IAM Identity Center redirects the customer to the configured `applicationUrl`.
If `IDENTITY_CENTER` is set, IAM Identity Center uses SAML identity-provider initiated authentication to sign the customer directly into a SAML-based application.

## Attribute Reference

This resource exports the following attributes in addition to the arguments above:

* `applicationAccount` - AWS account ID.
* `applicationArn` - ARN of the application.
* `id` - ARN of the application.
* `tagsAll` - Map of tags assigned to the resource, including those inherited from the provider [`defaultTags` configuration block](/docs/providers/aws/index.html#default_tags-configuration-block).

## Import

In Terraform v1.5.0 and later, use an [`import` block](https://developer.hashicorp.com/terraform/language/import) to import SSO Admin Application using the `id`. For example:

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

Using `terraform import`, import SSO Admin Application using the `id`. For example:

```console
% terraform import aws_ssoadmin_application.example arn:aws:sso::012345678901:application/id-12345678
```

<!-- cache-key: cdktf-0.20.0 input-75e45c35e2650f7bfc4e9876e51e95841b21e3d6246f328c36407311c3248a9c -->