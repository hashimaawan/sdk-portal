# Coordinates

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkNvb3JkaW5hdGVz

geographical coordinates of the stop

*This model accepts additional fields of type Any.*


# Class Name

`Coordinates`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `lat` | `float` | Optional | latitude |
| `lon` | `float` | Optional | longitude |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from furkottrips.models.coordinates import Coordinates

coordinates = Coordinates(
    lat=182.98,
    lon=16.08,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



