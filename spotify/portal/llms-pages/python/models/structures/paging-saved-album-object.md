# Paging Saved Album Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/python/x-redirect/JTI0bSUyRlBhZ2luZ1NhdmVkQWxidW1PYmplY3Q

*This model accepts additional fields of type Any.*


# Class Name

`PagingSavedAlbumObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `href` | `str` | Required | A link to the Web API endpoint returning the full result of the request |
| `limit` | `int` | Required | The maximum number of items in the response (as set in the query or by default). |
| `next` | `str` | Required | URL to the next page of items. ( `null` if none) |
| `offset` | `int` | Required | The offset of the items returned (as set in the query or by default) |
| `previous` | `str` | Required | URL to the previous page of items. ( `null` if none) |
| `total` | `int` | Required | The total number of items available to return. |
| `items` | [`List[SavedAlbumObject]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/models/structures/saved-album-object.md) | Required | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from spotifywebapiwithfixesandimprovementsfromsonallux.models.album_object import AlbumObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.album_restriction_object import AlbumRestrictionObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.album_type import AlbumType
from spotifywebapiwithfixesandimprovementsfromsonallux.models.copyright_object import CopyrightObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.external_id_object import ExternalIdObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.external_url_object import ExternalUrlObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.image_object import ImageObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.mtype import Type
from spotifywebapiwithfixesandimprovementsfromsonallux.models.paging_saved_album_object import PagingSavedAlbumObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.paging_simplified_track_object import PagingSimplifiedTrackObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.reason import Reason
from spotifywebapiwithfixesandimprovementsfromsonallux.models.release_date_precision import ReleaseDatePrecision
from spotifywebapiwithfixesandimprovementsfromsonallux.models.saved_album_object import SavedAlbumObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.simplified_artist_object import SimplifiedArtistObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.simplified_track_object import SimplifiedTrackObject

paging_saved_album_object = PagingSavedAlbumObject(
    href='https://api.spotify.com/v1/me/shows?offset=0&limit=20\n',
    limit=20,
    next='https://api.spotify.com/v1/me/shows?offset=1&limit=1',
    offset=0,
    previous='https://api.spotify.com/v1/me/shows?offset=1&limit=1',
    total=4,
    items=[
        SavedAlbumObject(
            added_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            album=AlbumObject(
                album_type=AlbumType.SINGLE,
                total_tracks=170,
                available_markets=[
                    'available_markets2',
                    'available_markets3'
                ],
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
                        url='url6',
                        height=182,
                        width=222,
                        additional_properties={
                            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                        }
                    )
                ],
                name='name8',
                release_date='release_date6',
                release_date_precision=ReleaseDatePrecision.DAY,
                uri='uri2',
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
                    ),
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
                tracks=PagingSimplifiedTrackObject(
                    href='href6',
                    limit=142,
                    next='next8',
                    offset=238,
                    previous='previous2',
                    total=236,
                    items=[
                        SimplifiedTrackObject(
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
                            available_markets=[
                                'available_markets2'
                            ],
                            disc_number=244,
                            duration_ms=52,
                            explicit=False,
                            additional_properties={
                                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                            }
                        )
                    ],
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                ),
                copyrights=[
                    CopyrightObject(
                        text='text2',
                        mtype='type2',
                        additional_properties={
                            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                        }
                    ),
                    CopyrightObject(
                        text='text2',
                        mtype='type2',
                        additional_properties={
                            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                        }
                    )
                ],
                external_ids=ExternalIdObject(
                    isrc='isrc8',
                    ean='ean8',
                    upc='upc2',
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                ),
                genres=[
                    'genres5',
                    'genres6',
                    'genres7'
                ],
                label='label8',
                popularity=78,
                restrictions=AlbumRestrictionObject(
                    reason=Reason.EXPLICIT,
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                ),
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



