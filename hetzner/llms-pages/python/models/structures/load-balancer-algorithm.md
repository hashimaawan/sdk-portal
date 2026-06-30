# Load Balancer Algorithm

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlckFsZ29yaXRobQ

Algorithm of the Load Balancer


# Class Name

`LoadBalancerAlgorithm`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `mtype` | [`Type28Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/enumerations/type-28.md) | Required | Type of the algorithm |


# Example

```python
from hetznercloudapi.models.load_balancer_algorithm import LoadBalancerAlgorithm
from hetznercloudapi.models.type_28_enum import Type28Enum

load_balancer_algorithm = LoadBalancerAlgorithm(
    mtype=Type28Enum.ROUND_ROBIN
)
```



