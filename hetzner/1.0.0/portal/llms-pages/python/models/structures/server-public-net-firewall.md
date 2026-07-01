# Server Public Net Firewall

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlNlcnZlclB1YmxpY05ldEZpcmV3YWxs

*This model accepts additional fields of type Any.*


# Class Name

`ServerPublicNetFirewall`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Optional | ID of the Resource |
| `status` | [`Status72`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/enumerations/status-72.md) | Optional | Status of the Firewall on the Server |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.server_public_net_firewall import ServerPublicNetFirewall
from hetznercloudapi.models.status_72 import Status72

server_public_net_firewall = ServerPublicNetFirewall(
    id=42,
    status=Status72.APPLIED,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



