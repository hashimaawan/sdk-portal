# Pages 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlBhZ2VzMQ

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Pages1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `first` | `str` | Optional | URI of the first page of the results. |
| `prev` | `str` | Optional | URI of the previous page of the results. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.pages_1 import Pages1

pages_1 = Pages1(
    first='https://api.digitalocean.com/v2/images?page=1',
    prev='https://api.digitalocean.com/v2/images?page=1',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



