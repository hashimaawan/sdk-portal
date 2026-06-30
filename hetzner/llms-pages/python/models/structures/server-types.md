# Server Types

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRlNlcnZlclR5cGVz

The Server types the Datacenter can handle


# Class Name

`ServerTypes`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `available` | `List[float]` | Required | IDs of Server types that are supported and for which the Datacenter has enough resources left |
| `available_for_migration` | `List[float]` | Required | IDs of Server types that are supported and for which the Datacenter has enough resources left |
| `supported` | `List[float]` | Required | IDs of Server types that are supported in the Datacenter |


# Example

```python
from hetznercloudapi.models.server_types import ServerTypes

server_types = ServerTypes(
    available=[
        1,
        2,
        3
    ],
    available_for_migration=[
        1,
        2,
        3
    ],
    supported=[
        1,
        2,
        3
    ]
)
```



