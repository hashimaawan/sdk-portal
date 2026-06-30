# Update Network Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRlVwZGF0ZU5ldHdvcmtSZXF1ZXN0


# Class Name

`UpdateNetworkRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `labels` | [`Labels2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/labels-2.md) | Optional | User-defined labels (key-value pairs) |
| `name` | `str` | Optional | New network name |


# Example

```python
from hetznercloudapi.models.labels_2 import Labels2
from hetznercloudapi.models.update_network_request import UpdateNetworkRequest

update_network_request = UpdateNetworkRequest(
    labels=Labels2(
        labelkey='labelkey4'
    ),
    name='new-name'
)
```



