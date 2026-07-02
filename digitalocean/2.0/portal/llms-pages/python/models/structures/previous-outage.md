# Previous Outage

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlByZXZpb3VzT3V0YWdl

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`PreviousOutage`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `duration_seconds` | `int` | Optional | - |
| `ended_at` | `str` | Optional | - |
| `region` | `str` | Optional | - |
| `started_at` | `str` | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.previous_outage import PreviousOutage

previous_outage = PreviousOutage(
    duration_seconds=120,
    ended_at='2022-03-17T18:06:55Z',
    region='us_east',
    started_at='2022-03-17T18:04:55Z',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



