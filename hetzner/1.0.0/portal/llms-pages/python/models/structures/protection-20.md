# Protection 20

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlByb3RlY3Rpb24yMA

Protection configuration for the Server

*This model accepts additional fields of type Any.*


# Class Name

`Protection20`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `delete` | `bool` | Required | If true, prevents the Server from being deleted |
| `rebuild` | `bool` | Required | If true, prevents the Server from being rebuilt |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.protection_20 import Protection20

protection_20 = Protection20(
    delete=False,
    rebuild=False,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



