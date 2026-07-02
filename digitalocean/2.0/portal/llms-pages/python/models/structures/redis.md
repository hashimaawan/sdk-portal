# Redis

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlJlZGlz

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Redis`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `regions` | `List[str]` | Optional, Read-only | An array of strings containing the names of available regions |
| `versions` | `List[str]` | Optional, Read-only | An array of strings containing the names of available regions |
| `layouts` | [`List[Layout]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/layout.md) | Optional, Read-only | An array of objects, each indicating the node sizes (otherwise referred to as slugs) that are available with various numbers of nodes in the database cluster. Each slugs denotes the node's identifier, CPU, and RAM (in that order). |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.layout import Layout
from digitaloceanapi.models.redis import Redis

redis = Redis(
    regions=[
        'ams3',
        'blr1'
    ],
    versions=[
        '4.4',
        '5.0'
    ],
    layouts=[
        Layout(
            num_nodes=190,
            sizes=[
                'sizes2',
                'sizes3'
            ],
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



