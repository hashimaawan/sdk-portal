# Progress 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlByb2dyZXNzMg

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`Progress2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `steps` | [`Array[StepsOfAnAlertSProgress]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/steps-of-an-alert-s-progress.md) | Optional | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
progress2 = Progress2.new(
  steps: [
    StepsOfAnAlertSProgress.new(
      ended_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
      name: 'name2',
      reason: Reason.new(
        code: 'code2',
        message: 'message4',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      started_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
      status: Status2::SUCCESS,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    StepsOfAnAlertSProgress.new(
      ended_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
      name: 'name2',
      reason: Reason.new(
        code: 'code2',
        message: 'message4',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      started_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
      status: Status2::SUCCESS,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



