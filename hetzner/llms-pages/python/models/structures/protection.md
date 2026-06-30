# Protection

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRlByb3RlY3Rpb24

Protection configuration for the Resource


# Class Name

`Protection`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `delete` | `bool` | Required | If true, prevents the Resource from being deleted |


# Example

```python
from hetznercloudapi.models.protection import Protection

protection = Protection(
    delete=False
)
```



