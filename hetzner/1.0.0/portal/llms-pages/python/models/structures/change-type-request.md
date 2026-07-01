# Change Type Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkNoYW5nZVR5cGVSZXF1ZXN0


# Class Name

`ChangeTypeRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `load_balancer_type` | `str` | Required | ID or name of Load Balancer type the Load Balancer should migrate to |


# Example

```python
from hetznercloudapi.models.change_type_request import ChangeTypeRequest

change_type_request = ChangeTypeRequest(
    load_balancer_type='lb21'
)
```



