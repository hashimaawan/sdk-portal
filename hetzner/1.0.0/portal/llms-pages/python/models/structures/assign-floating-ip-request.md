# Assign Floating IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkFzc2lnbkZsb2F0aW5nSVBSZXF1ZXN0

#### Call specific error codes

| Code                          | Description                                                   |
|------------------------------ |-------------------------------------------------------------- |
| `floating_ip_assigned`        | The floating IP is already assigned                           |

*This model accepts additional fields of type Any.*


# Class Name

`AssignFloatingIpRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `server` | `int` | Required | ID of the Server the Floating IP shall be assigned to |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.assign_floating_ip_request import AssignFloatingIpRequest

assign_floating_ip_request = AssignFloatingIpRequest(
    server=42,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



