# Play History Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/python/x-redirect/JTI0bSUyRlBsYXlIaXN0b3J5T2JqZWN0

*This model accepts additional fields of type Any.*


# Class Name

`PlayHistoryObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `track` | [`TrackObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/models/structures/track-object.md) | Optional | The track the user listened to. |
| `played_at` | `datetime` | Optional | The date and time the track was played. |
| `context` | [`ContextObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/models/structures/context-object.md) | Optional | The context the track was played from. |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from spotifywebapiwithfixesandimprovementsfromsonallux.models.album_restriction_object import AlbumRestrictionObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.album_type import AlbumType
from spotifywebapiwithfixesandimprovementsfromsonallux.models.artist_object import ArtistObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.context_object import ContextObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.external_url_object import ExternalUrlObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.followers_object import FollowersObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.image_object import ImageObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.mtype import Type
from spotifywebapiwithfixesandimprovementsfromsonallux.models.play_history_object import PlayHistoryObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.reason import Reason
from spotifywebapiwithfixesandimprovementsfromsonallux.models.release_date_precision import ReleaseDatePrecision
from spotifywebapiwithfixesandimprovementsfromsonallux.models.simplified_album_object import SimplifiedAlbumObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.simplified_artist_object import SimplifiedArtistObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.track_object import TrackObject

play_history_object = PlayHistoryObject(
    track=TrackObject(
        album=SimplifiedAlbumObject(
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
        artists=[
            ArtistObject(
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
                    'genres7',
                    'genres8'
                ],
                href='href2',
                id='id0',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            )
        ],
        available_markets=[
            'available_markets8'
        ],
        disc_number=206,
        duration_ms=142,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    played_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    context=ContextObject(
        mtype='type8',
        href='href4',
        external_urls=ExternalUrlObject(
            spotify='spotify6',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        uri='uri6',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



