# Acl Configuration 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkFjbENvbmZpZ3VyYXRpb24x

*This model accepts additional fields of type Object.*


# Class Name

`AclConfiguration1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `s_3_acl_option` | [`S3AclOption1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/enumerations/s3-acl-option-1.md) | Required | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
acl_configuration1 = AclConfiguration1.new(
  s3_acl_option: S3AclOption1::BUCKET_OWNER_FULL_CONTROL,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



