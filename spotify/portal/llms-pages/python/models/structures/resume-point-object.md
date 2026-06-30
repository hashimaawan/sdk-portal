# Resume Point Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/python/x-redirect/JTI0bSUyRlJlc3VtZVBvaW50T2JqZWN0

*This model accepts additional fields of type Any.*


# Class Name

`ResumePointObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `fully_played` | `bool` | Optional | Whether or not the episode has been fully played by the user. |
| `resume_position_ms` | `int` | Optional | The user's most recent position in the episode in milliseconds. |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from spotifywebapiwithfixesandimprovementsfromsonallux.models.resume_point_object import ResumePointObject

resume_point_object = ResumePointObject(
    fully_played=False,
    resume_position_ms=36,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



