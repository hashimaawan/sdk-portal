# Reserve to Region 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlJlc2VydmUlMjUyMHRvJTI1MjBSZWdpb24x

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`ReserveToRegion1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `project_id` | `uuid\|str` | Optional | The UUID of the project to which the reserved IP will be assigned. |
| `region` | `str` | Required | The slug identifier for the region the reserved IP will be reserved to. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.reserve_to_region_1 import ReserveToRegion1

reserve_to_region_1 = ReserveToRegion1(
    region='nyc3',
    project_id='746c6152-2fa2-11ed-92d3-27aaa54e4988',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



