# Show Base

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/python/x-redirect/JTI0bSUyRlNob3dCYXNl

*This model accepts additional fields of type Any.*


# Class Name

`ShowBase`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `available_markets` | `List[str]` | Required | A list of the countries in which the show can be played, identified by their [ISO 3166-1 alpha-2](http://en.wikipedia.org/wiki/ISO_3166-1_alpha-2) code. |
| `copyrights` | [`List[CopyrightObject]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/python/models/structures/copyright-object.md) | Required | The copyright statements of the show. |
| `description` | `str` | Required | A description of the show. HTML tags are stripped away from this field, use `html_description` field in case HTML tags are needed. |
| `html_description` | `str` | Required | A description of the show. This field may contain HTML tags. |
| `explicit` | `bool` | Required | Whether or not the show has explicit content (true = yes it does; false = no it does not OR unknown). |
| `external_urls` | [`ExternalUrlObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/python/models/structures/external-url-object.md) | Required | External URLs for this show. |
| `href` | `str` | Required | A link to the Web API endpoint providing full details of the show. |
| `id` | `str` | Required | The [Spotify ID](/documentation/web-api/concepts/spotify-uris-ids) for the show. |
| `images` | [`List[ImageObject]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/python/models/structures/image-object.md) | Required | The cover art for the show in various sizes, widest first. |
| `is_externally_hosted` | `bool` | Required | True if all of the shows episodes are hosted outside of Spotify's CDN. This field might be `null` in some cases. |
| `languages` | `List[str]` | Required | A list of the languages used in the show, identified by their [ISO 639](https://en.wikipedia.org/wiki/ISO_639) code. |
| `media_type` | `str` | Required | The media type of the show. |
| `name` | `str` | Required | The name of the episode. |
| `publisher` | `str` | Required | The publisher of the show. |
| `mtype` | `str` | Required, Constant | The object type.<br><br>**Value**: `"show"` |
| `uri` | `str` | Required | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for the show. |
| `total_episodes` | `int` | Required | The total number of episodes in the show. |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from spotifywebapiwithfixesandimprovementsfromsonallux.models.copyright_object import CopyrightObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.external_url_object import ExternalUrlObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.image_object import ImageObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.show_base import ShowBase

show_base = ShowBase(
    available_markets=[
        'available_markets0',
        'available_markets1',
        'available_markets2'
    ],
    copyrights=[
        CopyrightObject(
            text='text2',
            mtype='type2',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    description='description6',
    html_description='html_description6',
    explicit=False,
    external_urls=ExternalUrlObject(
        spotify='spotify6',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    href='href8',
    id='id6',
    images=[
        ImageObject(
            url='https://i.scdn.co/image/ab67616d00001e02ff9ca10b55ce82ae553c8228\n',
            height=300,
            width=300,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    is_externally_hosted=False,
    languages=[
        'languages3',
        'languages4',
        'languages5'
    ],
    media_type='media_type4',
    name='name6',
    publisher='publisher4',
    uri='uri0',
    total_episodes=6,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



