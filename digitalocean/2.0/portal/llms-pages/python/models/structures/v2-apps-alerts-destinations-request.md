# V2 Apps Alerts Destinations Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBBbGVydHMlMjUyMERlc3RpbmF0aW9ucyUyNTIwUmVxdWVzdA

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2AppsAlertsDestinationsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `emails` | `List[str]` | Optional | - |
| `slack_webhooks` | [`List[SlackWebhooksToSendAlertsTo]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/slack-webhooks-to-send-alerts-to.md) | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.slack_webhooks_to_send_alerts_to import SlackWebhooksToSendAlertsTo
from digitaloceanapi.models.v_2_apps_alerts_destinations_request import V2AppsAlertsDestinationsRequest

v_2_apps_alerts_destinations_request = V2AppsAlertsDestinationsRequest(
    emails=[
        'sammy@digitalocean.com'
    ],
    slack_webhooks=[
        SlackWebhooksToSendAlertsTo(
            channel='channel8',
            url='url0',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



