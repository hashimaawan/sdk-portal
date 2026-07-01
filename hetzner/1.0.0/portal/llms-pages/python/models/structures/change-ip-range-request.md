# Change IP Range Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkNoYW5nZUlQUmFuZ2VSZXF1ZXN0

*This model accepts additional fields of type Any.*


# Class Name

`ChangeIpRangeRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ip_range` | `str` | Required | The new prefix for the whole Network |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.change_ip_range_request import ChangeIpRangeRequest

change_ip_range_request = ChangeIpRangeRequest(
    ip_range='10.0.0.0/12',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



