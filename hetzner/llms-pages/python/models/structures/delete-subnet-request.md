# Delete Subnet Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRkRlbGV0ZVN1Ym5ldFJlcXVlc3Q


# Class Name

`DeleteSubnetRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ip_range` | `str` | Required | IP range of subnet to delete |


# Example

```python
from hetznercloudapi.models.delete_subnet_request import DeleteSubnetRequest

delete_subnet_request = DeleteSubnetRequest(
    ip_range='10.0.1.0/24'
)
```



