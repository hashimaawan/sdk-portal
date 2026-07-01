# Placement Group Nullable

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlBsYWNlbWVudEdyb3VwTnVsbGFibGU

*This model accepts additional fields of type Any.*


# Class Name

`PlacementGroupNullable`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `created` | `str` | Required | Point in time when the Resource was created (in ISO-8601 format) |
| `id` | `int` | Required | ID of the Resource |
| `labels` | `Dict[str, str]` | Required | User-defined labels (key-value pairs) |
| `name` | `str` | Required | Name of the Resource. Must be unique per Project. |
| `servers` | `List[int]` | Required | Array of IDs of Servers that are part of this Placement Group |
| `mtype` | `str` | Required, Constant | Type of the Placement Group<br><br>**Value**: `"spread"` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.placement_group_nullable import PlacementGroupNullable

placement_group_nullable = PlacementGroupNullable(
    created='2016-01-30T23:55:00+00:00',
    id=42,
    labels={
        'key0': 'labels2',
        'key1': 'labels3',
        'key2': 'labels4'
    },
    name='my-resource',
    servers=[
        42
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



