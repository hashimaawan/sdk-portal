# Route

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlJvdXRl

route leading to the stop

*This model accepts additional fields of type Any.*


# Class Name

`Route`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `distance` | `int` | Optional | route distance in meters |
| `duration` | `int` | Optional | route duration in seconds |
| `mode` | [`Mode`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/python/models/enumerations/mode.md) | Optional | travel mode |
| `polyline` | `str` | Optional | route path compatible with Google polyline encoding algorithm |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from furkottrips.models.mode import Mode
from furkottrips.models.route import Route

route = Route(
    distance=134,
    duration=168,
    mode=Mode.CAR,
    polyline='polyline0',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



