# Slack

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlNsYWNr

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`Slack`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `channel` | `String` | Required | Slack channel to notify of an alert trigger. |
| `url` | `String` | Required | Slack Webhook URL. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
slack = Slack.new(
  channel: 'Production Alerts',
  url: 'https://hooks.slack.com/services/T1234567/AAAAAAAA/ZZZZZZ',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



