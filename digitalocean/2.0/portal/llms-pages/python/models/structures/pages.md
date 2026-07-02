# Pages

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlBhZ2Vz

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Pages`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `last` | `str` | Optional | URI of the last page of the results. |
| `next` | `str` | Optional | URI of the next page of the results. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.pages import Pages

pages = Pages(
    last='https://api.digitalocean.com/v2/images?page=2',
    next='https://api.digitalocean.com/v2/images?page=2',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



