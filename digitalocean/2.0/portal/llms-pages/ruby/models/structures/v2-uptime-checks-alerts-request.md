# V2 Uptime Checks Alerts Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBVcHRpbWUlMjUyMENoZWNrcyUyNTIwQWxlcnRzJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2UptimeChecksAlertsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `comparison` | [`Comparison`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/enumerations/comparison.md) | Optional | The comparison operator used against the alert's threshold. |
| `name` | `String` | Optional | A human-friendly display name. |
| `notifications` | [`Notifications`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/notifications.md) | Optional | The notification settings for a trigger alert. |
| `period` | [`Period`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/enumerations/period.md) | Optional | Period of time the threshold must be exceeded to trigger the alert. |
| `threshold` | `Integer` | Optional | The threshold at which the alert will enter a trigger state. The specific threshold is dependent on the alert type. |
| `type` | [`Type20`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/enumerations/type-20.md) | Optional | The type of alert. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_uptime_checks_alerts_request = V2UptimeChecksAlertsRequest.new(
  comparison: Comparison::GREATER_THAN,
  name: 'Landing page degraded performance',
  notifications: Notifications.new(
    email: [
      'email4',
      'email3'
    ],
    slack: [
      Slack.new(
        channel: 'channel6',
        url: 'url2',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      Slack.new(
        channel: 'channel6',
        url: 'url2',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      Slack.new(
        channel: 'channel6',
        url: 'url2',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      )
    ],
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  period: Period::ENUM_2M,
  threshold: 300,
  type: Type20::LATENCY,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



