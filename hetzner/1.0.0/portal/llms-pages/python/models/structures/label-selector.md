# Label Selector

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkxhYmVsU2VsZWN0b3I

*This model accepts additional fields of type Any.*


# Class Name

`LabelSelector`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `selector` | `str` | Required | Label selector |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.label_selector import LabelSelector

label_selector = LabelSelector(
    selector='env=prod',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



