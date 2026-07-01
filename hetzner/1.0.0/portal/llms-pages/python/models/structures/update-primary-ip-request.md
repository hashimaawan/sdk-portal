# Update Primary IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlVwZGF0ZVByaW1hcnlJUFJlcXVlc3Q

*This model accepts additional fields of type Any.*


# Class Name

`UpdatePrimaryIpRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `auto_delete` | `bool` | Optional | Delete this Primary IP when the resource it is assigned to is deleted |
| `labels` | `Any` | Optional | User-defined labels (key-value pairs) |
| `name` | `str` | Optional | New unique name to set |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.update_primary_ip_request import UpdatePrimaryIpRequest

update_primary_ip_request = UpdatePrimaryIpRequest(
    auto_delete=True,
    labels=jsonpickle.decode('{"labelkey":"value"}'),
    name='my-ip',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



