# Server Backup

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlNlcnZlckJhY2t1cA

Will increase base Server costs by specific percentage

*This model accepts additional fields of type Any.*


# Class Name

`ServerBackup`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `percentage` | `str` | Required | Percentage by how much the base price will increase |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.server_backup import ServerBackup

server_backup = ServerBackup(
    percentage='20.0000000000',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



