# Change Protection Request 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkNoYW5nZVByb3RlY3Rpb25SZXF1ZXN0Mg

*This model accepts additional fields of type Any.*


# Class Name

`ChangeProtectionRequest2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `delete` | `bool` | Optional | If true, prevents the Primary IP from being deleted |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.change_protection_request_2 import ChangeProtectionRequest2

change_protection_request_2 = ChangeProtectionRequest2(
    delete=True,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



