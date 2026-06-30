# Search Items

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/php/x-redirect/JTI0bSUyRlNlYXJjaEl0ZW1z

*This model accepts additional fields of type array.*


# Class Name

`SearchItems`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `tracks` | [`?PagingTrackObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/php/models/structures/paging-track-object.md) | Optional | - | getTracks(): ?PagingTrackObject | setTracks(?PagingTrackObject tracks): void |
| `artists` | [`?PagingArtistObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/php/models/structures/paging-artist-object.md) | Optional | - | getArtists(): ?PagingArtistObject | setArtists(?PagingArtistObject artists): void |
| `albums` | [`?PagingSimplifiedAlbumObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/php/models/structures/paging-simplified-album-object.md) | Optional | - | getAlbums(): ?PagingSimplifiedAlbumObject | setAlbums(?PagingSimplifiedAlbumObject albums): void |
| `playlists` | [`?PagingPlaylistObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/php/models/structures/paging-playlist-object.md) | Optional | - | getPlaylists(): ?PagingPlaylistObject | setPlaylists(?PagingPlaylistObject playlists): void |
| `shows` | [`?PagingSimplifiedShowObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/php/models/structures/paging-simplified-show-object.md) | Optional | - | getShows(): ?PagingSimplifiedShowObject | setShows(?PagingSimplifiedShowObject shows): void |
| `episodes` | [`?PagingSimplifiedEpisodeObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/php/models/structures/paging-simplified-episode-object.md) | Optional | - | getEpisodes(): ?PagingSimplifiedEpisodeObject | setEpisodes(?PagingSimplifiedEpisodeObject episodes): void |
| `audiobooks` | [`?PagingSimplifiedAudiobookObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/php/models/structures/paging-simplified-audiobook-object.md) | Optional | - | getAudiobooks(): ?PagingSimplifiedAudiobookObject | setAudiobooks(?PagingSimplifiedAudiobookObject audiobooks): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\SearchItemsBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\PagingTrackObjectBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\TrackObjectBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\SimplifiedAlbumObjectBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\AlbumType;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\ExternalUrlObjectBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\ApiHelper;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\ImageObjectBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\ReleaseDatePrecision;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\SimplifiedArtistObjectBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Type;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\AlbumRestrictionObjectBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Reason;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\ArtistObjectBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\FollowersObjectBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\PagingArtistObjectBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\PagingSimplifiedAlbumObjectBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\PagingPlaylistObjectBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\SimplifiedPlaylistObjectBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\PagingSimplifiedShowObjectBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\ShowBaseBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\CopyrightObjectBuilder;

$searchItems = SearchItemsBuilder::init()
    ->tracks(
        PagingTrackObjectBuilder::init(
            'href6',
            142,
            238,
            236,
            [
                TrackObjectBuilder::init()
                    ->album(
                        SimplifiedAlbumObjectBuilder::init(
                            AlbumType::SINGLE,
                            170,
                            [
                                'available_markets2',
                                'available_markets3'
                            ],
                            ExternalUrlObjectBuilder::init()
                                ->spotify('spotify6')
                                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                ->build(),
                            'href0',
                            'id8',
                            [
                                ImageObjectBuilder::init(
                                    'url6'
                                )
                                    ->height(182)
                                    ->width(222)
                                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                    ->build()
                            ],
                            'name8',
                            'release_date6',
                            ReleaseDatePrecision::DAY,
                            'uri2',
                            [
                                SimplifiedArtistObjectBuilder::init()
                                    ->externalUrls(
                                        ExternalUrlObjectBuilder::init()
                                            ->spotify('spotify6')
                                            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                            ->build()
                                    )
                                    ->href('href2')
                                    ->id('id0')
                                    ->name('name0')
                                    ->type(Type::ARTIST)
                                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                    ->build(),
                                SimplifiedArtistObjectBuilder::init()
                                    ->externalUrls(
                                        ExternalUrlObjectBuilder::init()
                                            ->spotify('spotify6')
                                            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                            ->build()
                                    )
                                    ->href('href2')
                                    ->id('id0')
                                    ->name('name0')
                                    ->type(Type::ARTIST)
                                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                    ->build()
                            ]
                        )
                            ->restrictions(
                                AlbumRestrictionObjectBuilder::init()
                                    ->reason(Reason::EXPLICIT)
                                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                    ->build()
                            )
                            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                            ->build()
                    )
                    ->artists(
                        [
                            ArtistObjectBuilder::init()
                                ->externalUrls(
                                    ExternalUrlObjectBuilder::init()
                                        ->spotify('spotify6')
                                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                        ->build()
                                )
                                ->followers(
                                    FollowersObjectBuilder::init()
                                        ->href('href0')
                                        ->total(82)
                                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                        ->build()
                                )
                                ->genres(
                                    [
                                        'genres7',
                                        'genres8'
                                    ]
                                )
                                ->href('href2')
                                ->id('id0')
                                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                ->build()
                        ]
                    )
                    ->availableMarkets(
                        [
                            'available_markets2'
                        ]
                    )
                    ->discNumber(244)
                    ->durationMs(52)
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            ]
        )
            ->next('next8')
            ->previous('previous2')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->artists(
        PagingArtistObjectBuilder::init(
            'href2',
            214,
            54,
            52,
            [
                ArtistObjectBuilder::init()
                    ->externalUrls(
                        ExternalUrlObjectBuilder::init()
                            ->spotify('spotify6')
                            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                            ->build()
                    )
                    ->followers(
                        FollowersObjectBuilder::init()
                            ->href('href0')
                            ->total(82)
                            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                            ->build()
                    )
                    ->genres(
                        [
                            'genres5',
                            'genres6'
                        ]
                    )
                    ->href('href0')
                    ->id('id8')
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build(),
                ArtistObjectBuilder::init()
                    ->externalUrls(
                        ExternalUrlObjectBuilder::init()
                            ->spotify('spotify6')
                            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                            ->build()
                    )
                    ->followers(
                        FollowersObjectBuilder::init()
                            ->href('href0')
                            ->total(82)
                            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                            ->build()
                    )
                    ->genres(
                        [
                            'genres5',
                            'genres6'
                        ]
                    )
                    ->href('href0')
                    ->id('id8')
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build(),
                ArtistObjectBuilder::init()
                    ->externalUrls(
                        ExternalUrlObjectBuilder::init()
                            ->spotify('spotify6')
                            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                            ->build()
                    )
                    ->followers(
                        FollowersObjectBuilder::init()
                            ->href('href0')
                            ->total(82)
                            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                            ->build()
                    )
                    ->genres(
                        [
                            'genres5',
                            'genres6'
                        ]
                    )
                    ->href('href0')
                    ->id('id8')
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            ]
        )
            ->next('next2')
            ->previous('previous8')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->albums(
        PagingSimplifiedAlbumObjectBuilder::init(
            'href0',
            0,
            96,
            94,
            [
                SimplifiedAlbumObjectBuilder::init(
                    AlbumType::ALBUM,
                    196,
                    [
                        'available_markets2'
                    ],
                    ExternalUrlObjectBuilder::init()
                        ->spotify('spotify6')
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build(),
                    'href0',
                    'id8',
                    [
                        ImageObjectBuilder::init(
                            'url6'
                        )
                            ->height(182)
                            ->width(222)
                            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                            ->build(),
                        ImageObjectBuilder::init(
                            'url6'
                        )
                            ->height(182)
                            ->width(222)
                            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                            ->build()
                    ],
                    'name8',
                    'release_date6',
                    ReleaseDatePrecision::MONTH,
                    'uri2',
                    [
                        SimplifiedArtistObjectBuilder::init()
                            ->externalUrls(
                                ExternalUrlObjectBuilder::init()
                                    ->spotify('spotify6')
                                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                    ->build()
                            )
                            ->href('href2')
                            ->id('id0')
                            ->name('name0')
                            ->type(Type::ARTIST)
                            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                            ->build()
                    ]
                )
                    ->restrictions(
                        AlbumRestrictionObjectBuilder::init()
                            ->reason(Reason::EXPLICIT)
                            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                            ->build()
                    )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            ]
        )
            ->next('next4')
            ->previous('previous6')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->playlists(
        PagingPlaylistObjectBuilder::init(
            'href2',
            68,
            164,
            162,
            [
                SimplifiedPlaylistObjectBuilder::init()
                    ->collaborative(false)
                    ->description('description2')
                    ->externalUrls(
                        ExternalUrlObjectBuilder::init()
                            ->spotify('spotify6')
                            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                            ->build()
                    )
                    ->href('href0')
                    ->id('id8')
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build(),
                SimplifiedPlaylistObjectBuilder::init()
                    ->collaborative(false)
                    ->description('description2')
                    ->externalUrls(
                        ExternalUrlObjectBuilder::init()
                            ->spotify('spotify6')
                            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                            ->build()
                    )
                    ->href('href0')
                    ->id('id8')
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build(),
                SimplifiedPlaylistObjectBuilder::init()
                    ->collaborative(false)
                    ->description('description2')
                    ->externalUrls(
                        ExternalUrlObjectBuilder::init()
                            ->spotify('spotify6')
                            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                            ->build()
                    )
                    ->href('href0')
                    ->id('id8')
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            ]
        )
            ->next('next2')
            ->previous('previous8')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->shows(
        PagingSimplifiedShowObjectBuilder::init(
            'href0',
            248,
            88,
            86,
            [
                ShowBaseBuilder::init(
                    [
                        'available_markets2'
                    ],
                    [
                        CopyrightObjectBuilder::init()
                            ->text('text2')
                            ->type('type2')
                            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                            ->build()
                    ],
                    'description2',
                    'html_description2',
                    false,
                    ExternalUrlObjectBuilder::init()
                        ->spotify('spotify6')
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build(),
                    'href0',
                    'id8',
                    [
                        ImageObjectBuilder::init(
                            'url6'
                        )
                            ->height(182)
                            ->width(222)
                            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                            ->build(),
                        ImageObjectBuilder::init(
                            'url6'
                        )
                            ->height(182)
                            ->width(222)
                            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                            ->build()
                    ],
                    false,
                    [
                        'languages5'
                    ],
                    'media_type4',
                    'name8',
                    'publisher4',
                    'uri2',
                    166
                )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build(),
                ShowBaseBuilder::init(
                    [
                        'available_markets2'
                    ],
                    [
                        CopyrightObjectBuilder::init()
                            ->text('text2')
                            ->type('type2')
                            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                            ->build()
                    ],
                    'description2',
                    'html_description2',
                    false,
                    ExternalUrlObjectBuilder::init()
                        ->spotify('spotify6')
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build(),
                    'href0',
                    'id8',
                    [
                        ImageObjectBuilder::init(
                            'url6'
                        )
                            ->height(182)
                            ->width(222)
                            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                            ->build(),
                        ImageObjectBuilder::init(
                            'url6'
                        )
                            ->height(182)
                            ->width(222)
                            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                            ->build()
                    ],
                    false,
                    [
                        'languages5'
                    ],
                    'media_type4',
                    'name8',
                    'publisher4',
                    'uri2',
                    166
                )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build(),
                ShowBaseBuilder::init(
                    [
                        'available_markets2'
                    ],
                    [
                        CopyrightObjectBuilder::init()
                            ->text('text2')
                            ->type('type2')
                            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                            ->build()
                    ],
                    'description2',
                    'html_description2',
                    false,
                    ExternalUrlObjectBuilder::init()
                        ->spotify('spotify6')
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build(),
                    'href0',
                    'id8',
                    [
                        ImageObjectBuilder::init(
                            'url6'
                        )
                            ->height(182)
                            ->width(222)
                            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                            ->build(),
                        ImageObjectBuilder::init(
                            'url6'
                        )
                            ->height(182)
                            ->width(222)
                            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                            ->build()
                    ],
                    false,
                    [
                        'languages5'
                    ],
                    'media_type4',
                    'name8',
                    'publisher4',
                    'uri2',
                    166
                )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            ]
        )
            ->next('next6')
            ->previous('previous6')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



