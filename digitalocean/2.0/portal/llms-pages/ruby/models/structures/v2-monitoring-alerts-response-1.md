# V2 Monitoring Alerts Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBNb25pdG9yaW5nJTI1MjBBbGVydHMlMjUyMFJlc3BvbnNlMQ

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2MonitoringAlertsResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `policy` | [`Policy`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/policy.md) | Optional | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_monitoring_alerts_response1 = V2MonitoringAlertsResponse1.new(
  policy: Policy.new(
    alerts: Alerts.new(
      email: [
        'email2',
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
    compare: Compare::GREATERTHAN,
    description: 'description4',
    enabled: false,
    entities: [
      'entities9'
    ],
    tags: [
      'tags9',
      'tags0',
      'tags1'
    ],
    type: Type17::ENUM_V1INSIGHTSDROPLETDISK_READ,
    uuid: 'uuid0',
    value: 149.36,
    window: Window1::ENUM_30M,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



