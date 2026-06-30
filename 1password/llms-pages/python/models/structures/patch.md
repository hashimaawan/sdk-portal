# Patch

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/python/x-redirect/JTI0bSUyRlBhdGNo

*This model accepts additional fields of type Any.*


# Class Name

`Patch`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `op` | [`Op`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/python/models/enumerations/op.md) | Required | - |
| `path` | `str` | Required | An RFC6901 JSON Pointer pointing to the Item document, an Item Attribute, and Item Field by Field ID, or an Item Field Attribute |
| `value` | `Any` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from m1passwordconnect.models.op import Op
from m1passwordconnect.models.patch import Patch

patch = Patch(
    op=Op.REMOVE,
    path='/fields/06gnn2b95example10q91512p5/label',
    value=jsonpickle.decode('{"key1":"val1","key2":"val2"}'),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



