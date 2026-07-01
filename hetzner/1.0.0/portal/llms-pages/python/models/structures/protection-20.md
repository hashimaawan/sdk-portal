# Protection 20

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlByb3RlY3Rpb24yMA

Protection configuration for the Server


# Class Name

`Protection20`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `delete` | `bool` | Required | If true, prevents the Server from being deleted |
| `rebuild` | `bool` | Required | If true, prevents the Server from being rebuilt |


# Example

```python
from hetznercloudapi.models.protection_20 import Protection20

protection_20 = Protection20(
    delete=False,
    rebuild=False
)
```



