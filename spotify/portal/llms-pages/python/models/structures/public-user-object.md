# Public User Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/python/x-redirect/JTI0bSUyRlB1YmxpY1VzZXJPYmplY3Q

*This model accepts additional fields of type Any.*


# Class Name

`PublicUserObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `display_name` | `str` | Optional | The name displayed on the user's profile. `null` if not available. |
| `external_urls` | [`ExternalUrlObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/models/structures/external-url-object.md) | Optional | Known public external URLs for this user. |
| `followers` | [`FollowersObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/models/structures/followers-object.md) | Optional | Information about the followers of this user. |
| `href` | `str` | Optional | A link to the Web API endpoint for this user. |
| `id` | `str` | Optional | The [Spotify user ID](/documentation/web-api/concepts/spotify-uris-ids) for this user. |
| `images` | [`List[ImageObject]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/models/structures/image-object.md) | Optional | The user's profile image. |
| `mtype` | [`Type3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/models/enumerations/type-3.md) | Optional | The object type. |
| `uri` | `str` | Optional | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for this user. |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from spotifywebapiwithfixesandimprovementsfromsonallux.models.external_url_object import ExternalUrlObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.followers_object import FollowersObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.public_user_object import PublicUserObject

public_user_object = PublicUserObject(
    display_name='display_name8',
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
    href='href0',
    id='id8',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



