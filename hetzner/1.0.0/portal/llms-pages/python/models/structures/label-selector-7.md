# Label Selector 7

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkxhYmVsU2VsZWN0b3I3

Label selector and a list of selected targets

*This model accepts additional fields of type Any.*


# Class Name

`LabelSelector7`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `selector` | `str` | Required | Label selector |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.label_selector_7 import LabelSelector7

label_selector_7 = LabelSelector7(
    selector='env=prod',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



