# Forwarding Rule

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRkZvcndhcmRpbmdSdWxl

An object specifying a forwarding rule for a load balancer.

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`ForwardingRule`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `certificate_id` | `str` | Optional | The ID of the TLS certificate used for SSL termination if enabled. |
| `entry_port` | `int` | Required | An integer representing the port on which the load balancer instance will listen. |
| `entry_protocol` | [`EntryProtocol`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/entry-protocol.md) | Required | The protocol used for traffic to the load balancer. The possible values are: `http`, `https`, `http2`, `http3`, `tcp`, or `udp`. If you set the  `entry_protocol` to `udp`, the `target_protocol` must be set to `udp`.  When using UDP, the load balancer requires that you set up a health  check with a port that uses TCP, HTTP, or HTTPS to work properly. |
| `target_port` | `int` | Required | An integer representing the port on the backend Droplets to which the load balancer will send traffic. |
| `target_protocol` | [`TargetProtocol`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/target-protocol.md) | Required | The protocol used for traffic from the load balancer to the backend Droplets. The possible values are: `http`, `https`, `http2`, `tcp`, or `udp`. If you set the `target_protocol` to `udp`, the `entry_protocol` must be set to  `udp`. When using UDP, the load balancer requires that you set up a health  check with a port that uses TCP, HTTP, or HTTPS to work properly. |
| `tls_passthrough` | `bool` | Optional | A boolean value indicating whether SSL encrypted traffic will be passed through to the backend Droplets. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.entry_protocol import EntryProtocol
from digitaloceanapi.models.forwarding_rule import ForwardingRule
from digitaloceanapi.models.target_protocol import TargetProtocol

forwarding_rule = ForwardingRule(
    entry_port=443,
    entry_protocol=EntryProtocol.HTTPS,
    target_port=80,
    target_protocol=TargetProtocol.HTTP,
    certificate_id='892071a0-bb95-49bc-8021-3afd67a210bf',
    tls_passthrough=False,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



