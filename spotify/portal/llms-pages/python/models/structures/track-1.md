# Track 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/python/x-redirect/JTI0bSUyRlRyYWNrMQ

*This model accepts additional fields of type Any.*


# Class Name

`Track1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `uri` | `str` | Optional | Spotify URI |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from spotifywebapiwithfixesandimprovementsfromsonallux.models.track_1 import Track1

track_1 = Track1(
    uri='uri0',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



