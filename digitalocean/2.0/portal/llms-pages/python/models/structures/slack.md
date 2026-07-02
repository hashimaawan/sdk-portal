# Slack

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlNsYWNr

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Slack`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `channel` | `str` | Required | Slack channel to notify of an alert trigger. |
| `url` | `str` | Required | Slack Webhook URL. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.slack import Slack

slack = Slack(
    channel='Production Alerts',
    url='https://hooks.slack.com/services/T1234567/AAAAAAAA/ZZZZZZ',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



