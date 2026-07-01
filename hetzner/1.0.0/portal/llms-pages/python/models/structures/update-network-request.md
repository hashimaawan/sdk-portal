# Update Network Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlVwZGF0ZU5ldHdvcmtSZXF1ZXN0

*This model accepts additional fields of type Any.*


# Class Name

`UpdateNetworkRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `labels` | [`Labels2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/labels-2.md) | Optional | User-defined labels (key-value pairs) |
| `name` | `str` | Optional | New network name |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.labels_2 import Labels2
from hetznercloudapi.models.update_network_request import UpdateNetworkRequest

update_network_request = UpdateNetworkRequest(
    labels=Labels2(
        labelkey='labelkey4',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    name='new-name',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



