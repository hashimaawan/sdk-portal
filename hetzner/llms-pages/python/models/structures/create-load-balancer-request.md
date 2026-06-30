# Create Load Balancer Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRkNyZWF0ZUxvYWRCYWxhbmNlclJlcXVlc3Q


# Class Name

`CreateLoadBalancerRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `algorithm` | [`LoadBalancerAlgorithm`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/load-balancer-algorithm.md) | Required | Algorithm of the Load Balancer |
| `labels` | [`Labels`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/labels.md) | Optional | User-defined labels (key-value pairs) |
| `load_balancer_type` | `str` | Required | ID or name of the Load Balancer type this Load Balancer should be created with |
| `location` | `str` | Optional | ID or name of Location to create Load Balancer in |
| `name` | `str` | Required | Name of the Load Balancer |
| `network` | `int` | Optional | ID of the network the Load Balancer should be attached to on creation |
| `network_zone` | `str` | Optional | Name of network zone |
| `public_interface` | `bool` | Optional | Enable or disable the public interface of the Load Balancer |
| `services` | [`List[LoadBalancerService]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/load-balancer-service.md) | Optional | Array of services |
| `targets` | [`List[LoadBalancerTarget]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/load-balancer-target.md) | Optional | Array of targets |


# Example

```python
from hetznercloudapi.models.create_load_balancer_request import CreateLoadBalancerRequest
from hetznercloudapi.models.labels import Labels
from hetznercloudapi.models.load_balancer_algorithm import LoadBalancerAlgorithm
from hetznercloudapi.models.type_28_enum import Type28Enum

create_load_balancer_request = CreateLoadBalancerRequest(
    algorithm=LoadBalancerAlgorithm(
        mtype=Type28Enum.ROUND_ROBIN
    ),
    load_balancer_type='lb11',
    name='Web Frontend',
    labels=Labels(
        labelkey='labelkey4'
    ),
    location='location8',
    network=123,
    network_zone='eu-central',
    public_interface=True
)
```



