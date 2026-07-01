# Algorithm

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkFsZ29yaXRobQ

Algorithm of the Load Balancer


# Class Name

`Algorithm`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `mtype` | [`Type28Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/enumerations/type-28.md) | Required | Type of the algorithm |


# Example

```python
from hetznercloudapi.models.algorithm import Algorithm
from hetznercloudapi.models.type_28_enum import Type28Enum

algorithm = Algorithm(
    mtype=Type28Enum.ROUND_ROBIN
)
```



