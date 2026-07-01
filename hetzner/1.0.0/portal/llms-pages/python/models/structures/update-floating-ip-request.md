# Update Floating IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlVwZGF0ZUZsb2F0aW5nSVBSZXF1ZXN0

*This model accepts additional fields of type Any.*


# Class Name

`UpdateFloatingIpRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `description` | `str` | Optional | New Description to set |
| `labels` | `Any` | Optional | User-defined labels (key-value pairs) |
| `name` | `str` | Optional | New unique name to set |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.update_floating_ip_request import UpdateFloatingIpRequest

update_floating_ip_request = UpdateFloatingIpRequest(
    description='Web Frontend',
    labels=jsonpickle.decode('{"labelkey":"value"}'),
    name='Web Frontend',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



