---
subcategory: "CloudFront"
layout: "aws"
page_title: "AWS: aws_cloudfront_function"
description: |-
  Provides a CloudFront Function data source.
---


<!-- Please do not edit this file, it is generated. -->
# aws_cloudfront_function

Provides information about a CloudFront Function.

## Example Usage

```python
# DO NOT EDIT. Code generated by 'cdktf convert' - Please report bugs at https://cdk.tf/bug
from constructs import Construct
from cdktf import VariableType, TerraformVariable, TerraformStack
#
# Provider bindings are generated by running `cdktf get`.
# See https://cdk.tf/provider-generation for more details.
#
from imports.aws.data_aws_cloudfront_function import DataAwsCloudfrontFunction
class MyConvertedCode(TerraformStack):
    def __init__(self, scope, name, *, stage):
        super().__init__(scope, name)
        # Terraform Variables are not always the best fit for getting inputs in the context of Terraform CDK.
        #     You can read more about this at https://cdk.tf/variables
        function_name = TerraformVariable(self, "function_name",
            type=VariableType.STRING
        )
        DataAwsCloudfrontFunction(self, "existing",
            name=function_name.string_value,
            stage=stage
        )
```

## Argument Reference

This data source supports the following arguments:

* `name` - (Required) Name of the CloudFront function.
* `stage` - (Required) Function’s stage, either `DEVELOPMENT` or `LIVE`.

## Attribute Reference

This data source exports the following attributes in addition to the arguments above:

* `arn` - ARN identifying your CloudFront Function.
* `code` - Source code of the function
* `comment` - Comment.
* `etag` - ETag hash of the function
* `last_modified_time` - When this resource was last modified.
* `runtime` - Identifier of the function's runtime.
* `status` - Status of the function. Can be `UNPUBLISHED`, `UNASSOCIATED` or `ASSOCIATED`.

<!-- cache-key: cdktf-0.20.0 input-91b978e70ce3fa4778a1e7fadb7052748a3a704504ddaff849ccb10b0b522561 -->