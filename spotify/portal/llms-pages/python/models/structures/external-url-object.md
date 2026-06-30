# External Url Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/python/x-redirect/JTI0bSUyRkV4dGVybmFsVXJsT2JqZWN0

*This model accepts additional fields of type Any.*


# Class Name

`ExternalUrlObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `spotify` | `str` | Optional | The [Spotify URL](/documentation/web-api/concepts/spotify-uris-ids) for the object. |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from spotifywebapiwithfixesandimprovementsfromsonallux.models.external_url_object import ExternalUrlObject

external_url_object = ExternalUrlObject(
    spotify='spotify4',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



