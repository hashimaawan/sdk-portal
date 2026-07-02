# Previous Outage

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlByZXZpb3VzT3V0YWdl

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`PreviousOutage`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `duration_seconds` | `Integer` | Optional | - |
| `ended_at` | `String` | Optional | - |
| `region` | `String` | Optional | - |
| `started_at` | `String` | Optional | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
previous_outage = PreviousOutage.new(
  duration_seconds: 120,
  ended_at: '2022-03-17T18:06:55Z',
  region: 'us_east',
  started_at: '2022-03-17T18:04:55Z',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



