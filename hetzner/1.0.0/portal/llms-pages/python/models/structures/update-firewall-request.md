# Update Firewall Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlVwZGF0ZUZpcmV3YWxsUmVxdWVzdA

*This model accepts additional fields of type Any.*


# Class Name

`UpdateFirewallRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `labels` | `Any` | Optional | User-defined labels (key-value pairs) |
| `name` | `str` | Optional | New Firewall name |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.update_firewall_request import UpdateFirewallRequest

update_firewall_request = UpdateFirewallRequest(
    labels=jsonpickle.decode('{"labelkey":"value"}'),
    name='new-name',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



