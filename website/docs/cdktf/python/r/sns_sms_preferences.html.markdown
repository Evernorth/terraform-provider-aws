---
subcategory: "SNS (Simple Notification)"
layout: "aws"
page_title: "AWS: aws_sns_sms_preferences"
description: |-
  Provides a way to set SNS SMS preferences.
---


<!-- Please do not edit this file, it is generated. -->
# Resource: aws_sns_sms_preferences

Provides a way to set SNS SMS preferences.

## Example Usage

```python
# DO NOT EDIT. Code generated by 'cdktf convert' - Please report bugs at https://cdk.tf/bug
from constructs import Construct
from cdktf import TerraformStack
#
# Provider bindings are generated by running `cdktf get`.
# See https://cdk.tf/provider-generation for more details.
#
from imports.aws.sns_sms_preferences import SnsSmsPreferences
class MyConvertedCode(TerraformStack):
    def __init__(self, scope, name):
        super().__init__(scope, name)
        SnsSmsPreferences(self, "update_sms_prefs")
```

## Argument Reference

This resource supports the following arguments:

* `monthly_spend_limit` - (Optional) The maximum amount in USD that you are willing to spend each month to send SMS messages.
* `delivery_status_iam_role_arn` - (Optional) The ARN of the IAM role that allows Amazon SNS to write logs about SMS deliveries in CloudWatch Logs.
* `delivery_status_success_sampling_rate` - (Optional) The percentage of successful SMS deliveries for which Amazon SNS will write logs in CloudWatch Logs. The value must be between 0 and 100.
* `default_sender_id` - (Optional) A string, such as your business brand, that is displayed as the sender on the receiving device.
* `default_sms_type` - (Optional) The type of SMS message that you will send by default. Possible values are: Promotional, Transactional
* `usage_report_s3_bucket` - (Optional) The name of the Amazon S3 bucket to receive daily SMS usage reports from Amazon SNS.

## Attribute Reference

This resource exports no additional attributes.

<!-- cache-key: cdktf-0.20.0 input-fb3841d6bcaa58c6f6663ac36ae2dd4fc2b84b493c3c7984f840593cb184fb68 -->