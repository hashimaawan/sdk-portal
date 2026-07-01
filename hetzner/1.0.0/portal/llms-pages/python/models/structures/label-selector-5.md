# Label Selector 5

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkxhYmVsU2VsZWN0b3I1

Configuration for type label_selector, required if type is `label_selector`

*This model accepts additional fields of type Any.*


# Class Name

`LabelSelector5`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `selector` | `str` | Required | Label selector |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.label_selector_5 import LabelSelector5

label_selector_5 = LabelSelector5(
    selector='env=prod',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



