# Result Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlJlc3VsdENvbmZpZ3VyYXRpb24

The location in Amazon S3 where query and calculation results are stored and the encryption option, if any, used for query and calculation results. These are known as "client-side settings". If workgroup settings override client-side settings, then the query uses the workgroup settings.

*This model accepts additional fields of type Object.*


# Class Name

`ResultConfiguration`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `output_location` | `String` | Optional | - |
| `encryption_configuration` | [`EncryptionConfiguration2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/encryption-configuration-2.md) | Optional | - |
| `expected_bucket_owner` | `String` | Optional | **Constraints**: *Minimum Length*: `12`, *Maximum Length*: `12`, *Pattern*: `^[0-9]+$` |
| `acl_configuration` | [`AclConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/acl-configuration-1.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
result_configuration = ResultConfiguration.new(
  output_location: 'OutputLocation8',
  encryption_configuration: EncryptionConfiguration2.new(
    encryption_option: EncryptionOption1::SSE_S3,
    kms_key: 'KmsKey6',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  expected_bucket_owner: 'ExpectedBucketOwner8',
  acl_configuration: AclConfiguration1.new(
    s3_acl_option: S3AclOption1::BUCKET_OWNER_FULL_CONTROL,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



