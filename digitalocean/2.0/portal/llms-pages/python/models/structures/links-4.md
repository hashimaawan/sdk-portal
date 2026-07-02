# Links 4

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRkxpbmtzNA

The links object contains the `self` object, which contains the resource relationship.

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Links4`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `mself` | `str` | Optional | A URI that can be used to retrieve the resource. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.links_4 import Links4

links_4 = Links4(
    mself='https://api.digitalocean.com/v2/droplets/13457723',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



