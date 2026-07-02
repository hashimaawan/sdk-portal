# Result Configuration 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlJlc3VsdENvbmZpZ3VyYXRpb24x


# Class Name

`ResultConfiguration1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `output_location` | `String` | Optional | - |
| `encryption_configuration` | [`EncryptionConfiguration2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/encryption-configuration-2.md) | Optional | - |
| `expected_bucket_owner` | `String` | Optional | **Constraints**: *Minimum Length*: `12`, *Maximum Length*: `12`, *Pattern*: `^[0-9]+$` |
| `acl_configuration` | [`AclConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/acl-configuration-1.md) | Optional | - |


# Example

```ruby
result_configuration1 = ResultConfiguration1.new(
  'OutputLocation8',
  EncryptionConfiguration2.new(
    EncryptionOption1Enum::SSE_S3,
    'KmsKey6'
  ),
  'ExpectedBucketOwner8',
  AclConfiguration1.new(
    S3AclOption1Enum::BUCKET_OWNER_FULL_CONTROL
  )
)
```



