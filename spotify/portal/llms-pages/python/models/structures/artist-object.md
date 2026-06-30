# Artist Object

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/python/x-redirect/JTI0bSUyRkFydGlzdE9iamVjdA

*This model accepts additional fields of type Any.*


# Class Name

`ArtistObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `external_urls` | [`ExternalUrlObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/python/models/structures/external-url-object.md) | Optional | Known external URLs for this artist. |
| `followers` | [`FollowersObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/python/models/structures/followers-object.md) | Optional | Information about the followers of the artist. |
| `genres` | `List[str]` | Optional | A list of the genres the artist is associated with. If not yet classified, the array is empty. |
| `href` | `str` | Optional | A link to the Web API endpoint providing full details of the artist. |
| `id` | `str` | Optional | The [Spotify ID](/documentation/web-api/concepts/spotify-uris-ids) for the artist. |
| `images` | [`List[ImageObject]`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/python/models/structures/image-object.md) | Optional | Images of the artist in various sizes, widest first. |
| `name` | `str` | Optional | The name of the artist. |
| `popularity` | `int` | Optional | The popularity of the artist. The value will be between 0 and 100, with 100 being the most popular. The artist's popularity is calculated from the popularity of all the artist's tracks. |
| `mtype` | [`Type`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/python/models/enumerations/type.md) | Optional | The object type. |
| `uri` | `str` | Optional | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for the artist. |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from spotifywebapiwithfixesandimprovementsfromsonallux.models.artist_object import ArtistObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.external_url_object import ExternalUrlObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.followers_object import FollowersObject

artist_object = ArtistObject(
    external_urls=ExternalUrlObject(
        spotify='spotify6',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    followers=FollowersObject(
        href='href0',
        total=82,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    genres=[
        'Prog rock',
        'Grunge'
    ],
    href='href8',
    id='id6',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



