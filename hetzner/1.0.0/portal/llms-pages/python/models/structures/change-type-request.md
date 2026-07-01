# Change Type Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkNoYW5nZVR5cGVSZXF1ZXN0

*This model accepts additional fields of type Any.*


# Class Name

`ChangeTypeRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `load_balancer_type` | `str` | Required | ID or name of Load Balancer type the Load Balancer should migrate to |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.change_type_request import ChangeTypeRequest

change_type_request = ChangeTypeRequest(
    load_balancer_type='lb21',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



