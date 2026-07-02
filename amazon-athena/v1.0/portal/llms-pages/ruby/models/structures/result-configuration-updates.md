# Result Configuration Updates

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlJlc3VsdENvbmZpZ3VyYXRpb25VcGRhdGVz

The information about the updates in the query results, such as output location and encryption configuration for the query results.


# Class Name

`ResultConfigurationUpdates`


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


# Example

```ruby
result_configuration_updates = ResultConfigurationUpdates.new(
  'OutputLocation0',
  false,
  EncryptionConfiguration2.new(
    EncryptionOption1Enum::SSE_S3,
    'KmsKey6'
  ),
  false,
  'ExpectedBucketOwner0',
  nil,
  AclConfiguration1.new(
    envrr
  )
)
```



