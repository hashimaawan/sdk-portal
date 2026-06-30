# Detach from Network Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRkRldGFjaEZyb21OZXR3b3JrUmVxdWVzdA


# Class Name

`DetachFromNetworkRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `network` | `int` | Required | ID of an existing network to detach the Server from |


# Example

```python
from hetznercloudapi.models.detach_from_network_request import DetachFromNetworkRequest

detach_from_network_request = DetachFromNetworkRequest(
    network=4711
)
```



