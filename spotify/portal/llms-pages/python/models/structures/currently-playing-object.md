# Currently Playing Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/python/x-redirect/JTI0bSUyRkN1cnJlbnRseVBsYXlpbmdPYmplY3Q

*This model accepts additional fields of type Any.*


# Class Name

`CurrentlyPlayingObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `context` | [`ContextObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/models/structures/context-object.md) | Optional | A Context Object. Can be `null`. |
| `timestamp` | `int` | Optional | Unix Millisecond Timestamp when data was fetched |
| `progress_ms` | `int` | Optional | Progress into the currently playing track or episode. Can be `null`. |
| `is_playing` | `bool` | Optional | If something is currently playing, return `true`. |
| `item` | [TrackObject](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/models/structures/track-object.md) \| [EpisodeObject](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/models/structures/episode-object.md) \| None | Optional | This is a container for one-of cases. |
| `currently_playing_type` | `str` | Optional | The object type of the currently playing item. Can be one of `track`, `episode`, `ad` or `unknown`. |
| `actions` | [`DisallowsObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/models/structures/disallows-object.md) | Optional | Allows to update the user interface based on which playback actions are available within the current context. |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from spotifywebapiwithfixesandimprovementsfromsonallux.models.album_restriction_object import AlbumRestrictionObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.album_type import AlbumType
from spotifywebapiwithfixesandimprovementsfromsonallux.models.artist_object import ArtistObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.context_object import ContextObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.currently_playing_object import CurrentlyPlayingObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.external_url_object import ExternalUrlObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.followers_object import FollowersObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.image_object import ImageObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.mtype import Type
from spotifywebapiwithfixesandimprovementsfromsonallux.models.reason import Reason
from spotifywebapiwithfixesandimprovementsfromsonallux.models.release_date_precision import ReleaseDatePrecision
from spotifywebapiwithfixesandimprovementsfromsonallux.models.simplified_album_object import SimplifiedAlbumObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.simplified_artist_object import SimplifiedArtistObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.track_object import TrackObject

currently_playing_object = CurrentlyPlayingObject(
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
    timestamp=226,
    progress_ms=198,
    is_playing=False,
    item=TrackObject(
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
            ),
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
            'available_markets6',
            'available_markets7'
        ],
        disc_number=30,
        duration_ms=222,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



