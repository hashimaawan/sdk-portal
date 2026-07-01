# Protection 11

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlByb3RlY3Rpb24xMQ

Protection configuration for the Network


# Class Name

`Protection11`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `delete` | `bool` | Required | If true, prevents the Network from being deleted |


# Example

```python
from hetznercloudapi.models.protection_11 import Protection11

protection_11 = Protection11(
    delete=False
)
```



