# Update Server Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlVwZGF0ZVNlcnZlclJlcXVlc3Q

*This model accepts additional fields of type Any.*


# Class Name

`UpdateServerRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `labels` | `Any` | Optional | User-defined labels (key-value pairs) |
| `name` | `str` | Optional | New name to set |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.update_server_request import UpdateServerRequest

update_server_request = UpdateServerRequest(
    labels=jsonpickle.decode('{"labelkey":"value"}'),
    name='my-server',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



