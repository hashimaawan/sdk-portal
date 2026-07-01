# Assign Primary IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkFzc2lnblByaW1hcnlJUFJlcXVlc3Q

*This model accepts additional fields of type Any.*


# Class Name

`AssignPrimaryIpRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `assignee_id` | `int` | Required | ID of a resource of type `assignee_type` |
| `assignee_type` | `str` | Required, Constant | Type of resource assigning the Primary IP to<br><br>**Value**: `"server"` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.assign_primary_ip_request import AssignPrimaryIpRequest

assign_primary_ip_request = AssignPrimaryIpRequest(
    assignee_id=4711,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



