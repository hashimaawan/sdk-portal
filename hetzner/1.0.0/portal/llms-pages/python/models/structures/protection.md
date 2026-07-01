# Protection

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlByb3RlY3Rpb24

Protection configuration for the Resource

*This model accepts additional fields of type Any.*


# Class Name

`Protection`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `delete` | `bool` | Required | If true, prevents the Resource from being deleted |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.protection import Protection

protection = Protection(
    delete=False,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



