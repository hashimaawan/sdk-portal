# Search Items

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/python/x-redirect/JTI0bSUyRlNlYXJjaEl0ZW1z

*This model accepts additional fields of type Any.*


# Class Name

`SearchItems`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `tracks` | [`PagingTrackObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/python/models/structures/paging-track-object.md) | Optional | - |
| `artists` | [`PagingArtistObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/python/models/structures/paging-artist-object.md) | Optional | - |
| `albums` | [`PagingSimplifiedAlbumObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/python/models/structures/paging-simplified-album-object.md) | Optional | - |
| `playlists` | [`PagingPlaylistObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/python/models/structures/paging-playlist-object.md) | Optional | - |
| `shows` | [`PagingSimplifiedShowObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/python/models/structures/paging-simplified-show-object.md) | Optional | - |
| `episodes` | [`PagingSimplifiedEpisodeObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/python/models/structures/paging-simplified-episode-object.md) | Optional | - |
| `audiobooks` | [`PagingSimplifiedAudiobookObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/python/models/structures/paging-simplified-audiobook-object.md) | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from spotifywebapiwithfixesandimprovementsfromsonallux.models.album_restriction_object import AlbumRestrictionObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.album_type import AlbumType
from spotifywebapiwithfixesandimprovementsfromsonallux.models.artist_object import ArtistObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.copyright_object import CopyrightObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.external_url_object import ExternalUrlObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.followers_object import FollowersObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.image_object import ImageObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.mtype import Type
from spotifywebapiwithfixesandimprovementsfromsonallux.models.paging_artist_object import PagingArtistObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.paging_playlist_object import PagingPlaylistObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.paging_simplified_album_object import PagingSimplifiedAlbumObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.paging_simplified_show_object import PagingSimplifiedShowObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.paging_track_object import PagingTrackObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.reason import Reason
from spotifywebapiwithfixesandimprovementsfromsonallux.models.release_date_precision import ReleaseDatePrecision
from spotifywebapiwithfixesandimprovementsfromsonallux.models.search_items import SearchItems
from spotifywebapiwithfixesandimprovementsfromsonallux.models.show_base import ShowBase
from spotifywebapiwithfixesandimprovementsfromsonallux.models.simplified_album_object import SimplifiedAlbumObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.simplified_artist_object import SimplifiedArtistObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.simplified_playlist_object import SimplifiedPlaylistObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.track_object import TrackObject

search_items = SearchItems(
    tracks=PagingTrackObject(
        href='href6',
        limit=142,
        next='next8',
        offset=238,
        previous='previous2',
        total=236,
        items=[
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
                    )
                ],
                available_markets=[
                    'available_markets2'
                ],
                disc_number=244,
                duration_ms=52,
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            )
        ],
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    artists=PagingArtistObject(
        href='href2',
        limit=214,
        next='next2',
        offset=54,
        previous='previous8',
        total=52,
        items=[
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
                    'genres5',
                    'genres6'
                ],
                href='href0',
                id='id8',
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
                    'genres5',
                    'genres6'
                ],
                href='href0',
                id='id8',
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
                    'genres5',
                    'genres6'
                ],
                href='href0',
                id='id8',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            )
        ],
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    albums=PagingSimplifiedAlbumObject(
        href='href0',
        limit=0,
        next='next4',
        offset=96,
        previous='previous6',
        total=94,
        items=[
            SimplifiedAlbumObject(
                album_type=AlbumType.ALBUM,
                total_tracks=196,
                available_markets=[
                    'available_markets2'
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
                    ),
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
                release_date_precision=ReleaseDatePrecision.MONTH,
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
        ],
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    playlists=PagingPlaylistObject(
        href='href2',
        limit=68,
        next='next2',
        offset=164,
        previous='previous8',
        total=162,
        items=[
            SimplifiedPlaylistObject(
                collaborative=False,
                description='description2',
                external_urls=ExternalUrlObject(
                    spotify='spotify6',
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                ),
                href='href0',
                id='id8',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            SimplifiedPlaylistObject(
                collaborative=False,
                description='description2',
                external_urls=ExternalUrlObject(
                    spotify='spotify6',
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                ),
                href='href0',
                id='id8',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            SimplifiedPlaylistObject(
                collaborative=False,
                description='description2',
                external_urls=ExternalUrlObject(
                    spotify='spotify6',
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
        ],
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    shows=PagingSimplifiedShowObject(
        href='href0',
        limit=248,
        next='next6',
        offset=88,
        previous='previous6',
        total=86,
        items=[
            ShowBase(
                available_markets=[
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
                description='description2',
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
                        url='url6',
                        height=182,
                        width=222,
                        additional_properties={
                            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                        }
                    ),
                    ImageObject(
                        url='url6',
                        height=182,
                        width=222,
                        additional_properties={
                            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                        }
                    )
                ],
                is_externally_hosted=False,
                languages=[
                    'languages5'
                ],
                media_type='media_type4',
                name='name8',
                publisher='publisher4',
                uri='uri2',
                total_episodes=166,
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            ShowBase(
                available_markets=[
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
                description='description2',
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
                        url='url6',
                        height=182,
                        width=222,
                        additional_properties={
                            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                        }
                    ),
                    ImageObject(
                        url='url6',
                        height=182,
                        width=222,
                        additional_properties={
                            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                        }
                    )
                ],
                is_externally_hosted=False,
                languages=[
                    'languages5'
                ],
                media_type='media_type4',
                name='name8',
                publisher='publisher4',
                uri='uri2',
                total_episodes=166,
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            ShowBase(
                available_markets=[
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
                description='description2',
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
                        url='url6',
                        height=182,
                        width=222,
                        additional_properties={
                            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                        }
                    ),
                    ImageObject(
                        url='url6',
                        height=182,
                        width=222,
                        additional_properties={
                            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                        }
                    )
                ],
                is_externally_hosted=False,
                languages=[
                    'languages5'
                ],
                media_type='media_type4',
                name='name8',
                publisher='publisher4',
                uri='uri2',
                total_episodes=166,
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            )
        ],
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



