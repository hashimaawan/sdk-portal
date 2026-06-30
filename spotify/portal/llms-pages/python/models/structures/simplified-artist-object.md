# Simplified Artist Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/python/x-redirect/JTI0bSUyRlNpbXBsaWZpZWRBcnRpc3RPYmplY3Q

*This model accepts additional fields of type Any.*


# Class Name

`SimplifiedArtistObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `external_urls` | [`ExternalUrlObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/models/structures/external-url-object.md) | Optional | Known external URLs for this artist. |
| `href` | `str` | Optional | A link to the Web API endpoint providing full details of the artist. |
| `id` | `str` | Optional | The [Spotify ID](/documentation/web-api/concepts/spotify-uris-ids) for the artist. |
| `name` | `str` | Optional | The name of the artist. |
| `mtype` | [`Type`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/models/enumerations/type.md) | Optional | The object type. |
| `uri` | `str` | Optional | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for the artist. |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from spotifywebapiwithfixesandimprovementsfromsonallux.models.external_url_object import ExternalUrlObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.mtype import Type
from spotifywebapiwithfixesandimprovementsfromsonallux.models.simplified_artist_object import SimplifiedArtistObject

simplified_artist_object = SimplifiedArtistObject(
    external_urls=ExternalUrlObject(
        spotify='spotify6',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    href='href6',
    id='id4',
    name='name4',
    mtype=Type.ARTIST,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



