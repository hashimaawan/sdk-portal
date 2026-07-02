# Encryption Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkVuY3J5cHRpb25Db25maWd1cmF0aW9u

If query and calculation results are encrypted in Amazon S3, indicates the encryption option used (for example, <code>SSE_KMS</code> or <code>CSE_KMS</code>) and key information.

*This model accepts additional fields of type Object.*


# Class Name

`EncryptionConfiguration`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `encryption_option` | [`EncryptionOption1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/enumerations/encryption-option-1.md) | Required | - |
| `kms_key` | `String` | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
encryption_configuration = EncryptionConfiguration.new(
  encryption_option: EncryptionOption1::SSE_KMS,
  kms_key: 'KmsKey4',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



