# Used By

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRlVzZWRCeQ


# Class Name

`UsedBy`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Required | ID of resource referenced |
| `mtype` | `str` | Required | Type of resource referenced |


# Example

```python
from hetznercloudapi.models.used_by import UsedBy

used_by = UsedBy(
    id=4711,
    mtype='load_balancer'
)
```



