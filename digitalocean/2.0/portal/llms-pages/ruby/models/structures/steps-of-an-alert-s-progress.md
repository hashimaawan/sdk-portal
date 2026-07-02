# Steps of an Alert S Progress

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlN0ZXBzJTI1MjBvZiUyNTIwYW4lMjUyMGFsZXJ0JTI1MjdzJTI1MjBwcm9ncmVzcy4

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`StepsOfAnAlertSProgress`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ended_at` | `DateTime` | Optional | - |
| `name` | `String` | Optional | - |
| `reason` | [`Reason`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/reason.md) | Optional | - |
| `started_at` | `DateTime` | Optional | - |
| `status` | [`Status2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/enumerations/status-2.md) | Optional | **Default**: `Status2::UNKNOWN` |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
steps_of_an_alert_s_progress = StepsOfAnAlertSProgress.new(
  ended_at: DateTimeHelper.from_rfc3339('2020-11-19T20:27:18Z'),
  name: 'example_step',
  reason: Reason.new(
    code: 'code2',
    message: 'message4',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  started_at: DateTimeHelper.from_rfc3339('2020-11-19T20:27:18Z'),
  status: Status2::SUCCESS,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



