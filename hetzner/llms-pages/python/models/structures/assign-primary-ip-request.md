# Assign Primary IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRkFzc2lnblByaW1hcnlJUFJlcXVlc3Q


# Class Name

`AssignPrimaryIPRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `assignee_id` | `int` | Required | ID of a resource of type `assignee_type` |
| `assignee_type` | `str` | Required, Constant | Type of resource assigning the Primary IP to<br><br>**Value**: `"server"` |


# Example

```python
from hetznercloudapi.models.assign_primary_ip_request import AssignPrimaryIPRequest

assign_primary_ip_request = AssignPrimaryIPRequest(
    assignee_id=4711
)
```



