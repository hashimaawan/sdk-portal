# Create Primary IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkNyZWF0ZVByaW1hcnlJUFJlcXVlc3Q

*This model accepts additional fields of type Any.*


# Class Name

`CreatePrimaryIpRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `assignee_id` | `int` | Optional | ID of the resource the Primary IP should be assigned to. Omitted if it should not be assigned. |
| `assignee_type` | `str` | Required, Constant | Resource type the Primary IP can be assigned to<br><br>**Value**: `"server"` |
| `auto_delete` | `bool` | Optional | Delete the Primary IP when the Server it is assigned to is deleted. If omitted defaults to `false`. |
| `datacenter` | `str` | Optional | ID or name of Datacenter the Primary IP will be bound to. Needs to be omitted if `assignee_id` is passed. |
| `labels` | `Any` | Optional | User-defined labels (key-value pairs) |
| `name` | `str` | Required | - |
| `mtype` | [`Type51`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/enumerations/type-51.md) | Required | Primary IP type |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.create_primary_ip_request import CreatePrimaryIpRequest
from hetznercloudapi.models.type_51 import Type51

create_primary_ip_request = CreatePrimaryIpRequest(
    name='my-ip',
    mtype=Type51.IPV4,
    assignee_id=17,
    auto_delete=False,
    datacenter='fsn1-dc8',
    labels=jsonpickle.decode('{"labelkey":"value"}'),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



