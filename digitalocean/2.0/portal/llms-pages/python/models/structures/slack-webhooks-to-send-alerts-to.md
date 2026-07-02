# Slack Webhooks to Send Alerts To

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlNsYWNrJTI1MjBXZWJob29rcyUyNTIwdG8lMjUyMHNlbmQlMjUyMGFsZXJ0cyUyNTIwdG8

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`SlackWebhooksToSendAlertsTo`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `channel` | `str` | Optional | - |
| `url` | `str` | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.slack_webhooks_to_send_alerts_to import SlackWebhooksToSendAlertsTo

slack_webhooks_to_send_alerts_to = SlackWebhooksToSendAlertsTo(
    channel='Channel Name',
    url='https://hooks.slack.com/services/T00000000/B00000000/XXXXXXXXXXXXXXXXXXXXXXXX',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



