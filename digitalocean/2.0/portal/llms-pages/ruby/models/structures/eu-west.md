# Eu West

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRkV1V2VzdA

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`EuWest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `status` | [`Status16`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/enumerations/status-16.md) | Optional | - |
| `status_changed_at` | `String` | Optional | - |
| `thirty_day_uptime_percentage` | `Float` | Optional | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
eu_west = EuWest.new(
  status: Status16::UP,
  status_changed_at: '2022-03-17T22:28:51Z',
  thirty_day_uptime_percentage: 97.99,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



