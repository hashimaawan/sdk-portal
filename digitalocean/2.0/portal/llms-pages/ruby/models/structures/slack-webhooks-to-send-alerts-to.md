# Slack Webhooks to Send Alerts To

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlNsYWNrJTI1MjBXZWJob29rcyUyNTIwdG8lMjUyMHNlbmQlMjUyMGFsZXJ0cyUyNTIwdG8

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`SlackWebhooksToSendAlertsTo`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `channel` | `String` | Optional | - |
| `url` | `String` | Optional | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
slack_webhooks_to_send_alerts_to = SlackWebhooksToSendAlertsTo.new(
  channel: 'Channel Name',
  url: 'https://hooks.slack.com/services/T00000000/B00000000/XXXXXXXXXXXXXXXXXXXXXXXX',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



