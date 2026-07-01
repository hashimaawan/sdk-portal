# Create Placement Group Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkNyZWF0ZVBsYWNlbWVudEdyb3VwUmVxdWVzdA

*This model accepts additional fields of type Any.*


# Class Name

`CreatePlacementGroupRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `labels` | `Any` | Optional | User-defined labels (key-value pairs) |
| `name` | `str` | Required | Name of the PlacementGroup |
| `mtype` | `str` | Required, Constant | Define the Placement Group Type.<br><br>**Value**: `"spread"` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.create_placement_group_request import CreatePlacementGroupRequest

create_placement_group_request = CreatePlacementGroupRequest(
    name='my Placement Group',
    labels=jsonpickle.decode('{"key1":"val1","key2":"val2"}'),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



