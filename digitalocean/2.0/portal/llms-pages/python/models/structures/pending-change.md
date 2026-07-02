# Pending Change

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlBlbmRpbmdDaGFuZ2U

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`PendingChange`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `droplet_id` | `int` | Optional | - |
| `removing` | `bool` | Optional | - |
| `status` | `str` | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.pending_change import PendingChange

pending_change = PendingChange(
    droplet_id=8043964,
    removing=False,
    status='waiting',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



