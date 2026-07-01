# Rebuild Server Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlJlYnVpbGRTZXJ2ZXJSZXF1ZXN0


# Class Name

`RebuildServerRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `image` | `str` | Required | ID or name of Image to rebuilt from. |


# Example

```python
from hetznercloudapi.models.rebuild_server_request import RebuildServerRequest

rebuild_server_request = RebuildServerRequest(
    image='ubuntu-20.04'
)
```



