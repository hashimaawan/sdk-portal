# Session Configuration 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlNlc3Npb25Db25maWd1cmF0aW9uMg

*This model accepts additional fields of type Object.*


# Class Name

`SessionConfiguration2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `execution_role` | `String` | Optional | **Constraints**: *Minimum Length*: `20`, *Maximum Length*: `2048`, *Pattern*: `^arn:aws[a-z\-]*:iam::\d{12}:role/?[a-zA-Z_0-9+=,.@\-_/]+$` |
| `working_directory` | `String` | Optional | - |
| `idle_timeout_seconds` | `Integer` | Optional | - |
| `encryption_configuration` | [`EncryptionConfiguration`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/encryption-configuration.md) | Optional | If query and calculation results are encrypted in Amazon S3, indicates the encryption option used (for example, <code>SSE_KMS</code> or <code>CSE_KMS</code>) and key information. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
session_configuration2 = SessionConfiguration2.new(
  execution_role: 'ExecutionRole4',
  working_directory: 'WorkingDirectory8',
  idle_timeout_seconds: 46,
  encryption_configuration: EncryptionConfiguration.new(
    encryption_option: EncryptionOption1::SSE_S3,
    kms_key: 'KmsKey6',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



