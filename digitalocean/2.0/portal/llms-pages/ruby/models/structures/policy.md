# Policy

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlBvbGljeQ

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`Policy`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `alerts` | [`Alerts`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/alerts.md) | Required | - |
| `compare` | [`Compare`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/enumerations/compare.md) | Required | - |
| `description` | `String` | Required | - |
| `enabled` | `TrueClass \| FalseClass` | Required | - |
| `entities` | `Array[String]` | Required | - |
| `tags` | `Array[String]` | Required | - |
| `type` | [`Type17`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/enumerations/type-17.md) | Required | - |
| `uuid` | `String` | Required | - |
| `value` | `Float` | Required | - |
| `window` | [`Window1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/enumerations/window-1.md) | Required | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
policy = Policy.new(
  alerts: Alerts.new(
    email: [
      'bob@exmaple.com'
    ],
    slack: [
      Slack.new(
        channel: 'Production Alerts',
        url: 'https://hooks.slack.com/services/T1234567/AAAAAAAA/ZZZZZZ',
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
  description: 'CPU Alert',
  enabled: true,
  entities: [
    '192018292'
  ],
  tags: [
    'droplet_tag'
  ],
  type: Type17::ENUM_V1INSIGHTSDROPLETCPU,
  uuid: '78b3da62-27e5-49ba-ac70-5db0b5935c64',
  value: 80,
  window: Window1::ENUM_5M,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



