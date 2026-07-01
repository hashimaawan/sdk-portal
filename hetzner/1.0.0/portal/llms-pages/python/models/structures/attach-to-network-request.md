# Attach to Network Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkF0dGFjaFRvTmV0d29ya1JlcXVlc3Q

*This model accepts additional fields of type Any.*


# Class Name

`AttachToNetworkRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `alias_ips` | `List[str]` | Optional | Additional IPs to be assigned to this Server |
| `ip` | `str` | Optional | IP to request to be assigned to this Server; if you do not provide this then you will be auto assigned an IP address |
| `network` | `int` | Required | ID of an existing network to attach the Server to |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.attach_to_network_request import AttachToNetworkRequest

attach_to_network_request = AttachToNetworkRequest(
    network=4711,
    alias_ips=[
        '10.0.1.2'
    ],
    ip='10.0.1.1',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



