# Assign Floating IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRkFzc2lnbkZsb2F0aW5nSVBSZXF1ZXN0

#### Call specific error codes

| Code                          | Description                                                   |
|------------------------------ |-------------------------------------------------------------- |
| `floating_ip_assigned`        | The floating IP is already assigned                           |


# Class Name

`AssignFloatingIPRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `server` | `int` | Required | ID of the Server the Floating IP shall be assigned to |


# Example

```python
from hetznercloudapi.models.assign_floating_ip_request import AssignFloatingIPRequest

assign_floating_ip_request = AssignFloatingIPRequest(
    server=42
)
```



