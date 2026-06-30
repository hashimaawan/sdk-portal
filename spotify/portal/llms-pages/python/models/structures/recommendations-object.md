# Recommendations Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/python/x-redirect/JTI0bSUyRlJlY29tbWVuZGF0aW9uc09iamVjdA

*This model accepts additional fields of type Any.*


# Class Name

`RecommendationsObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `seeds` | [`List[RecommendationSeedObject]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/models/structures/recommendation-seed-object.md) | Required | An array of recommendation seed objects. |
| `tracks` | [`List[TrackObject]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/python/models/structures/track-object.md) | Required | An array of track objects ordered according to the parameters supplied. |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from spotifywebapiwithfixesandimprovementsfromsonallux.models.album_restriction_object import AlbumRestrictionObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.album_type import AlbumType
from spotifywebapiwithfixesandimprovementsfromsonallux.models.artist_object import ArtistObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.external_url_object import ExternalUrlObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.followers_object import FollowersObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.image_object import ImageObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.mtype import Type
from spotifywebapiwithfixesandimprovementsfromsonallux.models.reason import Reason
from spotifywebapiwithfixesandimprovementsfromsonallux.models.recommendation_seed_object import RecommendationSeedObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.recommendations_object import RecommendationsObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.release_date_precision import ReleaseDatePrecision
from spotifywebapiwithfixesandimprovementsfromsonallux.models.simplified_album_object import SimplifiedAlbumObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.simplified_artist_object import SimplifiedArtistObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.track_object import TrackObject

recommendations_object = RecommendationsObject(
    seeds=[
        RecommendationSeedObject(
            after_filtering_size=36,
            after_relinking_size=144,
            href='href4',
            id='id2',
            initial_pool_size=42,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    tracks=[
        TrackObject(
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
                'available_markets8',
                'available_markets9'
            ],
            disc_number=168,
            duration_ms=232,
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



