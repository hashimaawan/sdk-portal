# Resource

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRlJlc291cmNl


# Class Name

`Resource`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Required | ID of the Resource |
| `mtype` | `str` | Required | Type of resource referenced |


# Example

```python
from hetznercloudapi.models.resource import Resource

resource = Resource(
    id=42,
    mtype='server'
)
```



