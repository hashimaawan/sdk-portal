# Datadog

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRkRhdGFkb2c

DataDog configuration.

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`Datadog`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `api_key` | `String` | Required | Datadog API key. |
| `endpoint` | `String` | Optional | Datadog HTTP log intake endpoint. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
datadog = Datadog.new(
  api_key: 'abcdefghijklmnopqrstuvwxyz0123456789',
  endpoint: 'https://mydatadogendpoint.com',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



