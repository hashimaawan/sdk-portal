# Change IP Range Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRkNoYW5nZUlQUmFuZ2VSZXF1ZXN0


# Class Name

`ChangeIPRangeRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ip_range` | `str` | Required | The new prefix for the whole Network |


# Example

```python
from hetznercloudapi.models.change_ip_range_request import ChangeIPRangeRequest

change_ip_range_request = ChangeIPRangeRequest(
    ip_range='10.0.0.0/12'
)
```



