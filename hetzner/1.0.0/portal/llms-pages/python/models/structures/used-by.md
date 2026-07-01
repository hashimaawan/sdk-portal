# Used By

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlVzZWRCeQ

*This model accepts additional fields of type Any.*


# Class Name

`UsedBy`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Required | ID of resource referenced |
| `mtype` | `str` | Required | Type of resource referenced |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.used_by import UsedBy

used_by = UsedBy(
    id=4711,
    mtype='load_balancer',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



