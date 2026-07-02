# V2 Droplets Actions Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBEcm9wbGV0cyUyNTIwQWN0aW9ucyUyNTIwUmVxdWVzdA

Specifies the action that will be taken on the Droplet.

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2DropletsActionsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `mtype` | [`Type12`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/type-12.md) | Required | The type of action to initiate for the Droplet. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.type_12 import Type12
from digitaloceanapi.models.v_2_droplets_actions_request import V2DropletsActionsRequest

v_2_droplets_actions_request = V2DropletsActionsRequest(
    mtype=Type12.REBOOT,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



