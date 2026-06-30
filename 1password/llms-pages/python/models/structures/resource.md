# Resource

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/python/x-redirect/JTI0bSUyRlJlc291cmNl

*This model accepts additional fields of type Any.*


# Class Name

`Resource`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `item` | [`Item2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/python/models/structures/item-2.md) | Optional | - |
| `item_version` | `int` | Optional | - |
| `mtype` | [`Type`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/python/models/enumerations/type.md) | Optional | - |
| `vault` | [`Vault3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/python/models/structures/vault-3.md) | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from m1passwordconnect.models.item_2 import Item2
from m1passwordconnect.models.mtype import Type
from m1passwordconnect.models.resource import Resource
from m1passwordconnect.models.vault_3 import Vault3

resource = Resource(
    item=Item2(
        id='id2',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    item_version=108,
    mtype=Type.ITEM,
    vault=Vault3(
        id='id6',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



