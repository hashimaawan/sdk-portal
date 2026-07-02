# Alert 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRkFsZXJ0MQ

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`Alert1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `component_name` | `String` | Optional | - |
| `emails` | `Array[String]` | Optional | - |
| `id` | `String` | Optional, Read-only | - |
| `phase` | [`Phase1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/enumerations/phase-1.md) | Optional | **Default**: `Phase1::UNKNOWN` |
| `progress` | [`Progress2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/progress-2.md) | Optional | - |
| `slack_webhooks` | [`Array[SlackWebhooksToSendAlertsTo]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/slack-webhooks-to-send-alerts-to.md) | Optional | - |
| `spec` | [`Alert`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/alert.md) | Optional | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
alert1 = Alert1.new(
  component_name: 'backend',
  emails: [
    'sammy@digitalocean.com'
  ],
  id: '4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf',
  phase: Phase1::ACTIVE,
  progress: Progress2.new(
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
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



