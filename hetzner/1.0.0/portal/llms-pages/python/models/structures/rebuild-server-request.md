# Rebuild Server Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlJlYnVpbGRTZXJ2ZXJSZXF1ZXN0

*This model accepts additional fields of type Any.*


# Class Name

`RebuildServerRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `image` | `str` | Required | ID or name of Image to rebuilt from. |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.rebuild_server_request import RebuildServerRequest

rebuild_server_request = RebuildServerRequest(
    image='ubuntu-20.04',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



