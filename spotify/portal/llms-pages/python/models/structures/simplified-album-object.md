# Simplified Album Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/python/x-redirect/JTI0bSUyRlNpbXBsaWZpZWRBbGJ1bU9iamVjdA

*This model accepts additional fields of type Any.*


# Class Name

`SimplifiedAlbumObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `album_type` | [`AlbumType`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/models/enumerations/album-type.md) | Required | The type of the album. |
| `total_tracks` | `int` | Required | The number of tracks in the album. |
| `available_markets` | `List[str]` | Required | The markets in which the album is available: [ISO 3166-1 alpha-2 country codes](http://en.wikipedia.org/wiki/ISO_3166-1_alpha-2). _**NOTE**: an album is considered available in a market when at least 1 of its tracks is available in that market._ |
| `external_urls` | [`ExternalUrlObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/models/structures/external-url-object.md) | Required | Known external URLs for this album. |
| `href` | `str` | Required | A link to the Web API endpoint providing full details of the album. |
| `id` | `str` | Required | The [Spotify ID](/documentation/web-api/concepts/spotify-uris-ids) for the album. |
| `images` | [`List[ImageObject]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/models/structures/image-object.md) | Required | The cover art for the album in various sizes, widest first. |
| `name` | `str` | Required | The name of the album. In case of an album takedown, the value may be an empty string. |
| `release_date` | `str` | Required | The date the album was first released. |
| `release_date_precision` | [`ReleaseDatePrecision`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/models/enumerations/release-date-precision.md) | Required | The precision with which `release_date` value is known. |
| `restrictions` | [`AlbumRestrictionObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/models/structures/album-restriction-object.md) | Optional | Included in the response when a content restriction is applied. |
| `mtype` | `str` | Required, Constant | The object type.<br><br>**Value**: `"album"` |
| `uri` | `str` | Required | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for the album. |
| `artists` | [`List[SimplifiedArtistObject]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/models/structures/simplified-artist-object.md) | Required | The artists of the album. Each artist object includes a link in `href` to more detailed information about the artist. |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from spotifywebapiwithfixesandimprovementsfromsonallux.models.album_restriction_object import AlbumRestrictionObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.album_type import AlbumType
from spotifywebapiwithfixesandimprovementsfromsonallux.models.external_url_object import ExternalUrlObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.image_object import ImageObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.mtype import Type
from spotifywebapiwithfixesandimprovementsfromsonallux.models.reason import Reason
from spotifywebapiwithfixesandimprovementsfromsonallux.models.release_date_precision import ReleaseDatePrecision
from spotifywebapiwithfixesandimprovementsfromsonallux.models.simplified_album_object import SimplifiedAlbumObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.simplified_artist_object import SimplifiedArtistObject

simplified_album_object = SimplifiedAlbumObject(
    album_type=AlbumType.COMPILATION,
    total_tracks=9,
    available_markets=[
        'CA',
        'BR',
        'IT'
    ],
    external_urls=ExternalUrlObject(
        spotify='spotify6',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    href='href4',
    id='2up3OPMp9Tb4dAKM2erWXQ',
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
    name='name2',
    release_date='1981-12',
    release_date_precision=ReleaseDatePrecision.YEAR,
    uri='spotify:album:2up3OPMp9Tb4dAKM2erWXQ',
    artists=[
        SimplifiedArtistObject(
            external_urls=ExternalUrlObject(
                spotify='spotify6',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            href='href2',
            id='id0',
            name='name0',
            mtype=Type.ARTIST,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    restrictions=AlbumRestrictionObject(
        reason=Reason.EXPLICIT,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



