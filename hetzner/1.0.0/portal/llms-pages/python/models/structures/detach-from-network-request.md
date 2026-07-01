# Detach from Network Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkRldGFjaEZyb21OZXR3b3JrUmVxdWVzdA

*This model accepts additional fields of type Any.*


# Class Name

`DetachFromNetworkRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `network` | `int` | Required | ID of an existing network to detach the Server from |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.detach_from_network_request import DetachFromNetworkRequest

detach_from_network_request = DetachFromNetworkRequest(
    network=4711,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



