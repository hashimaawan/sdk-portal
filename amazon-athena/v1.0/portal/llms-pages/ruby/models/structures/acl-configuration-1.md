# Acl Configuration 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkFjbENvbmZpZ3VyYXRpb24x


# Class Name

`AclConfiguration1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `s_3_acl_option` | [`S3AclOption1Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/enumerations/s3-acl-option-1.md) | Required | - |


# Example

```ruby
acl_configuration1 = AclConfiguration1.new(
  S3AclOption1Enum::BUCKET_OWNER_FULL_CONTROL
)
```



