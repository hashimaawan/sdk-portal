# Add to Placement Group Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkFkZFRvUGxhY2VtZW50R3JvdXBSZXF1ZXN0

*This model accepts additional fields of type Any.*


# Class Name

`AddToPlacementGroupRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `placement_group` | `int` | Required | ID of Placement Group the Server should be added to |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.add_to_placement_group_request import AddToPlacementGroupRequest

add_to_placement_group_request = AddToPlacementGroupRequest(
    placement_group=1,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



