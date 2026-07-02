# Links

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRkxpbmtz

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Links`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `pages` | [Pages](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/pages.md) \| [Pages1](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/pages-1.md) \| Any \| None | Optional | This is a container for any-of cases. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.links import Links
from digitaloceanapi.models.pages import Pages

links = Links(
    pages=Pages(
        last='last6',
        next='next2',
        additional_properties={
            'pages': jsonpickle.decode('{"first":"https://api.digitalocean.com/v2/account/keys?page=1","prev":"https://api.digitalocean.com/v2/account/keys?page=2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



