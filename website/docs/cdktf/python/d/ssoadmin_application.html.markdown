---
subcategory: "SSO Admin"
layout: "aws"
page_title: "AWS: aws_ssoadmin_application"
description: |-
  Terraform data source for managing an AWS SSO Admin Application.
---


<!-- Please do not edit this file, it is generated. -->
# Data Source: aws_ssoadmin_application

Terraform data source for managing an AWS SSO Admin Application.

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
from imports.aws.data_aws_ssoadmin_application import DataAwsSsoadminApplication
class MyConvertedCode(TerraformStack):
    def __init__(self, scope, name):
        super().__init__(scope, name)
        DataAwsSsoadminApplication(self, "example",
            application_arn="arn:aws:sso::012345678901:application/ssoins-1234/apl-5678"
        )
```

## Argument Reference

The following arguments are required:

* `application_arn` - (Required) ARN of the application.

## Attribute Reference

This data source exports the following attributes in addition to the arguments above:

* `application_account` - AWS account ID.
* `application_provider_arn` - ARN of the application provider.
* `description` - Description of the application.
* `id` - ARN of the application.
* `instance_arn` - ARN of the instance of IAM Identity Center.
* `name` - Name of the application.
* `portal_options` - Options for the portal associated with an application. See the `aws_ssoadmin_application` [resource documentation](../r/ssoadmin_application.html.markdown#portal_options-argument-reference). The attributes are the same.
* `status` - Status of the application.

<!-- cache-key: cdktf-0.20.0 input-0d07cfe6432527b9115d7fc49e2aad9b81dacbb2fee9606812ff5efd006c2f93 -->