# Trip

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlRyaXA

*This model accepts additional fields of type Any.*


# Class Name

`Trip`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `begin` | `datetime` | Optional | begin of the trip in its local timezone as YYYY-MM-DDThh:mm |
| `description` | `str` | Optional | description of the trip (truncated to 200 characters) |
| `end` | `datetime` | Optional | end of the trip in its local timezone as YYYY-MM-DDThh:mm |
| `id` | `str` | Optional | Unique ID of the trip |
| `name` | `str` | Optional | name of the trip |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from furkottrips.models.trip import Trip

trip = Trip(
    begin=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    description='description8',
    end=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    id='id8',
    name='name8',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



