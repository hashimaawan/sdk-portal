# Step

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/#/python/x-redirect/JTI0bSUyRlN0ZXA


# Class Name

`Step`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `address` | `str` | Optional | address of the stop |
| `arrival` | `datetime` | Optional | arrival at the stop in its local timezone as YYYY-MM-DDThh:mm |
| `coordinates` | [`Coordinates`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/llms-pages/python/models/structures/coordinates.md) | Optional | geographical coordinates of the stop |
| `departure` | `datetime` | Optional | departure from the stop in its local timezone as YYYY-MM-DDThh:mm |
| `name` | `str` | Optional | name of the stop |
| `nights` | `int` | Optional | number of nights |
| `passthru` | `bool` | Optional | true for pass-through points anchoring route |
| `route` | [`Route`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/llms-pages/python/models/structures/route.md) | Optional | route leading to the stop |
| `url` | `str` | Optional | url of the page with more information about the stop |


# Example

```python
import dateutil.parser

from furkottrips.models.coordinates import Coordinates
from furkottrips.models.step import Step

step = Step(
    address='address4',
    arrival=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    coordinates=Coordinates(
        lat=182.98,
        lon=16.08
    ),
    departure=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    name='name8'
)
```



