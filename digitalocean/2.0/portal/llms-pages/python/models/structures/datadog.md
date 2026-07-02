# Datadog

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRkRhdGFkb2c

DataDog configuration.

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Datadog`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `api_key` | `str` | Required | Datadog API key. |
| `endpoint` | `str` | Optional | Datadog HTTP log intake endpoint. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.datadog import Datadog

datadog = Datadog(
    api_key='abcdefghijklmnopqrstuvwxyz0123456789',
    endpoint='https://mydatadogendpoint.com',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



