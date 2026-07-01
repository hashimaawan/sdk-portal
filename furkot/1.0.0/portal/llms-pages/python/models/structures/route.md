# Route

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlJvdXRl

route leading to the stop


# Class Name

`Route`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `distance` | `int` | Optional | route distance in meters |
| `duration` | `int` | Optional | route duration in seconds |
| `mode` | [`ModeEnum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/python/models/enumerations/mode.md) | Optional | travel mode |
| `polyline` | `str` | Optional | route path compatible with Google polyline encoding algorithm |


# Example

```python
from furkottrips.models.mode_enum import ModeEnum
from furkottrips.models.route import Route

route = Route(
    distance=134,
    duration=168,
    mode=ModeEnum.CAR,
    polyline='polyline0'
)
```



