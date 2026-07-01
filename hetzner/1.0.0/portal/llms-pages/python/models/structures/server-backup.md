# Server Backup

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlNlcnZlckJhY2t1cA

Will increase base Server costs by specific percentage


# Class Name

`ServerBackup`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `percentage` | `str` | Required | Percentage by how much the base price will increase |


# Example

```python
from hetznercloudapi.models.server_backup import ServerBackup

server_backup = ServerBackup(
    percentage='20.0000000000'
)
```



