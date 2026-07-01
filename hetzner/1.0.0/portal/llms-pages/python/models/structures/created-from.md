# Created From

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkNyZWF0ZWRGcm9t

Information about the Server the Image was created from

*This model accepts additional fields of type Any.*


# Class Name

`CreatedFrom`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Required | ID of the Server the Image was created from |
| `name` | `str` | Required | Server name at the time the Image was created |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.created_from import CreatedFrom

created_from = CreatedFrom(
    id=1,
    name='Server',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



