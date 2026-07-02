# Result Configuration Updates 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlJlc3VsdENvbmZpZ3VyYXRpb25VcGRhdGVzMg

*This model accepts additional fields of type Object.*


# Class Name

`ResultConfigurationUpdates2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `output_location` | `String` | Optional | - |
| `remove_output_location` | `TrueClass \| FalseClass` | Optional | - |
| `encryption_configuration` | [`EncryptionConfiguration2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/encryption-configuration-2.md) | Optional | - |
| `remove_encryption_configuration` | `TrueClass \| FalseClass` | Optional | - |
| `expected_bucket_owner` | `String` | Optional | **Constraints**: *Minimum Length*: `12`, *Maximum Length*: `12`, *Pattern*: `^[0-9]+$` |
| `remove_expected_bucket_owner` | `TrueClass \| FalseClass` | Optional | - |
| `acl_configuration` | [`AclConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/acl-configuration-1.md) | Optional | - |
| `remove_acl_configuration` | `TrueClass \| FalseClass` | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
result_configuration_updates2 = ResultConfigurationUpdates2.new(
  output_location: 'OutputLocation0',
  remove_output_location: false,
  encryption_configuration: EncryptionConfiguration2.new(
    encryption_option: EncryptionOption1::SSE_S3,
    kms_key: 'KmsKey6',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  remove_encryption_configuration: false,
  expected_bucket_owner: 'ExpectedBucketOwner0',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



