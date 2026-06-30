# Many Albums

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/python/x-redirect/JTI0bSUyRk1hbnlBbGJ1bXM

*This model accepts additional fields of type Any.*


# Class Name

`ManyAlbums`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `albums` | [`List[AlbumObject]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/models/structures/album-object.md) | Required | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from spotifywebapiwithfixesandimprovementsfromsonallux.models.album_object import AlbumObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.album_restriction_object import AlbumRestrictionObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.album_type import AlbumType
from spotifywebapiwithfixesandimprovementsfromsonallux.models.copyright_object import CopyrightObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.external_id_object import ExternalIdObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.external_url_object import ExternalUrlObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.image_object import ImageObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.many_albums import ManyAlbums
from spotifywebapiwithfixesandimprovementsfromsonallux.models.mtype import Type
from spotifywebapiwithfixesandimprovementsfromsonallux.models.paging_simplified_track_object import PagingSimplifiedTrackObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.reason import Reason
from spotifywebapiwithfixesandimprovementsfromsonallux.models.release_date_precision import ReleaseDatePrecision
from spotifywebapiwithfixesandimprovementsfromsonallux.models.simplified_artist_object import SimplifiedArtistObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.simplified_track_object import SimplifiedTrackObject

many_albums = ManyAlbums(
    albums=[
        AlbumObject(
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
            href='href0',
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
            name='name8',
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
            tracks=PagingSimplifiedTrackObject(
                href='https://api.spotify.com/v1/me/shows?offset=0&limit=20\n',
                limit=20,
                next='https://api.spotify.com/v1/me/shows?offset=1&limit=1',
                offset=0,
                previous='https://api.spotify.com/v1/me/shows?offset=1&limit=1',
                total=4,
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
                'Egg punk',
                'Noise rock'
            ],
            label='label8',
            popularity=66,
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
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



