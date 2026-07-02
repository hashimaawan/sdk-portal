# V2 Apps Alerts Destinations Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBBbGVydHMlMjUyMERlc3RpbmF0aW9ucyUyNTIwUmVxdWVzdA

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2AppsAlertsDestinationsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `emails` | `Array[String]` | Optional | - |
| `slack_webhooks` | [`Array[SlackWebhooksToSendAlertsTo]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/slack-webhooks-to-send-alerts-to.md) | Optional | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_apps_alerts_destinations_request = V2AppsAlertsDestinationsRequest.new(
  emails: [
    'sammy@digitalocean.com'
  ],
  slack_webhooks: [
    SlackWebhooksToSendAlertsTo.new(
      channel: 'channel8',
      url: 'url0',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    SlackWebhooksToSendAlertsTo.new(
      channel: 'channel8',
      url: 'url0',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    SlackWebhooksToSendAlertsTo.new(
      channel: 'channel8',
      url: 'url0',
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



