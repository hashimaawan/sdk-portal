# Tier

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlRpZXI

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`Tier`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `build_seconds` | `String` | Optional | - |
| `egress_bandwidth_bytes` | `String` | Optional | - |
| `name` | `String` | Optional | - |
| `slug` | `String` | Optional | - |
| `storage_bytes` | `String` | Optional | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
tier = Tier.new(
  build_seconds: '233',
  egress_bandwidth_bytes: '123',
  name: 'test',
  slug: 'test',
  storage_bytes: '10000000',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



