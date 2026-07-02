# App Bandwidth Usage

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRkFwcEJhbmR3aWR0aFVzYWdl

Bandwidth usage for an app.

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`AppBandwidthUsage`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `app_id` | `String` | Optional | The ID of the app. |
| `bandwidth_bytes` | `String` | Optional | The used bandwidth amount in bytes. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
app_bandwidth_usage = AppBandwidthUsage.new(
  app_id: '4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf',
  bandwidth_bytes: '513668',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



