# Audiobook Base

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/python/x-redirect/JTI0bSUyRkF1ZGlvYm9va0Jhc2U

*This model accepts additional fields of type Any.*


# Class Name

`AudiobookBase`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `authors` | [`List[AuthorObject]`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/python/models/structures/author-object.md) | Required | The author(s) for the audiobook. |
| `available_markets` | `List[str]` | Required | A list of the countries in which the audiobook can be played, identified by their [ISO 3166-1 alpha-2](http://en.wikipedia.org/wiki/ISO_3166-1_alpha-2) code. |
| `copyrights` | [`List[CopyrightObject]`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/python/models/structures/copyright-object.md) | Required | The copyright statements of the audiobook. |
| `description` | `str` | Required | A description of the audiobook. HTML tags are stripped away from this field, use `html_description` field in case HTML tags are needed. |
| `html_description` | `str` | Required | A description of the audiobook. This field may contain HTML tags. |
| `edition` | `str` | Optional | The edition of the audiobook. |
| `explicit` | `bool` | Required | Whether or not the audiobook has explicit content (true = yes it does; false = no it does not OR unknown). |
| `external_urls` | [`ExternalUrlObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/python/models/structures/external-url-object.md) | Required | External URLs for this audiobook. |
| `href` | `str` | Required | A link to the Web API endpoint providing full details of the audiobook. |
| `id` | `str` | Required | The [Spotify ID](/documentation/web-api/concepts/spotify-uris-ids) for the audiobook. |
| `images` | [`List[ImageObject]`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/python/models/structures/image-object.md) | Required | The cover art for the audiobook in various sizes, widest first. |
| `languages` | `List[str]` | Required | A list of the languages used in the audiobook, identified by their [ISO 639](https://en.wikipedia.org/wiki/ISO_639) code. |
| `media_type` | `str` | Required | The media type of the audiobook. |
| `name` | `str` | Required | The name of the audiobook. |
| `narrators` | [`List[NarratorObject]`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/python/models/structures/narrator-object.md) | Required | The narrator(s) for the audiobook. |
| `publisher` | `str` | Required | The publisher of the audiobook. |
| `mtype` | `str` | Required, Constant | The object type.<br><br>**Value**: `"audiobook"` |
| `uri` | `str` | Required | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for the audiobook. |
| `total_chapters` | `int` | Required | The number of chapters in this audiobook. |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from spotifywebapiwithfixesandimprovementsfromsonallux.models.audiobook_base import AudiobookBase
from spotifywebapiwithfixesandimprovementsfromsonallux.models.author_object import AuthorObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.copyright_object import CopyrightObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.external_url_object import ExternalUrlObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.image_object import ImageObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.narrator_object import NarratorObject

audiobook_base = AudiobookBase(
    authors=[
        AuthorObject(
            name='name0',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    available_markets=[
        'available_markets2',
        'available_markets3'
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
    description='description8',
    html_description='html_description2',
    explicit=False,
    external_urls=ExternalUrlObject(
        spotify='spotify6',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    href='href0',
    id='id8',
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
    languages=[
        'languages5',
        'languages6'
    ],
    media_type='media_type4',
    name='name8',
    narrators=[
        NarratorObject(
            name='name0',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    publisher='publisher4',
    uri='uri2',
    total_chapters=106,
    edition='Unabridged',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



