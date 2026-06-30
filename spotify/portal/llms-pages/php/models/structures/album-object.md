# Album Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/php/x-redirect/JTI0bSUyRkFsYnVtT2JqZWN0

*This model accepts additional fields of type array.*


# Class Name

`AlbumObject`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `albumType` | [`string(AlbumType)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/php/models/enumerations/album-type.md) | Required | The type of the album. | getAlbumType(): string | setAlbumType(string albumType): void |
| `totalTracks` | `int` | Required | The number of tracks in the album. | getTotalTracks(): int | setTotalTracks(int totalTracks): void |
| `availableMarkets` | `string[]` | Required | The markets in which the album is available: [ISO 3166-1 alpha-2 country codes](http://en.wikipedia.org/wiki/ISO_3166-1_alpha-2). _**NOTE**: an album is considered available in a market when at least 1 of its tracks is available in that market._ | getAvailableMarkets(): array | setAvailableMarkets(array availableMarkets): void |
| `externalUrls` | [`ExternalUrlObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/php/models/structures/external-url-object.md) | Required | Known external URLs for this album. | getExternalUrls(): ExternalUrlObject | setExternalUrls(ExternalUrlObject externalUrls): void |
| `href` | `string` | Required | A link to the Web API endpoint providing full details of the album. | getHref(): string | setHref(string href): void |
| `id` | `string` | Required | The [Spotify ID](/documentation/web-api/concepts/spotify-uris-ids) for the album. | getId(): string | setId(string id): void |
| `images` | [`ImageObject[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/php/models/structures/image-object.md) | Required | The cover art for the album in various sizes, widest first. | getImages(): array | setImages(array images): void |
| `name` | `string` | Required | The name of the album. In case of an album takedown, the value may be an empty string. | getName(): string | setName(string name): void |
| `releaseDate` | `string` | Required | The date the album was first released. | getReleaseDate(): string | setReleaseDate(string releaseDate): void |
| `releaseDatePrecision` | [`string(ReleaseDatePrecision)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/php/models/enumerations/release-date-precision.md) | Required | The precision with which `release_date` value is known. | getReleaseDatePrecision(): string | setReleaseDatePrecision(string releaseDatePrecision): void |
| `restrictions` | [`?AlbumRestrictionObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/php/models/structures/album-restriction-object.md) | Optional | Included in the response when a content restriction is applied. | getRestrictions(): ?AlbumRestrictionObject | setRestrictions(?AlbumRestrictionObject restrictions): void |
| `type` | `string` | Required, Constant | The object type.<br><br>**Value**: `'album'` | getType(): string | setType(string type): void |
| `uri` | `string` | Required | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for the album. | getUri(): string | setUri(string uri): void |
| `artists` | [`SimplifiedArtistObject[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/php/models/structures/simplified-artist-object.md) | Required | The artists of the album. Each artist object includes a link in `href` to more detailed information about the artist. | getArtists(): array | setArtists(array artists): void |
| `tracks` | [`PagingSimplifiedTrackObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/php/models/structures/paging-simplified-track-object.md) | Required | The tracks of the album. | getTracks(): PagingSimplifiedTrackObject | setTracks(PagingSimplifiedTrackObject tracks): void |
| `copyrights` | [`CopyrightObject[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/php/models/structures/copyright-object.md) | Required | The copyright statements of the album. | getCopyrights(): array | setCopyrights(array copyrights): void |
| `externalIds` | [`ExternalIdObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/php/models/structures/external-id-object.md) | Required | Known external IDs for the album. | getExternalIds(): ExternalIdObject | setExternalIds(ExternalIdObject externalIds): void |
| `genres` | `string[]` | Required | A list of the genres the album is associated with. If not yet classified, the array is empty. | getGenres(): array | setGenres(array genres): void |
| `label` | `string` | Required | The label associated with the album. | getLabel(): string | setLabel(string label): void |
| `popularity` | `int` | Required | The popularity of the album. The value will be between 0 and 100, with 100 being the most popular. | getPopularity(): int | setPopularity(int popularity): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\AlbumObjectBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\AlbumType;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\ExternalUrlObjectBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\ApiHelper;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\ImageObjectBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\ReleaseDatePrecision;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\SimplifiedArtistObjectBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Type;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\PagingSimplifiedTrackObjectBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\SimplifiedTrackObjectBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\CopyrightObjectBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\ExternalIdObjectBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\AlbumRestrictionObjectBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Reason;

$albumObject = AlbumObjectBuilder::init(
    AlbumType::COMPILATION,
    9,
    [
        'CA',
        'BR',
        'IT'
    ],
    ExternalUrlObjectBuilder::init()
        ->spotify('spotify6')
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build(),
    'href8',
    '2up3OPMp9Tb4dAKM2erWXQ',
    [
        ImageObjectBuilder::init(
            'https://i.scdn.co/image/ab67616d00001e02ff9ca10b55ce82ae553c8228
'
        )
            ->height(300)
            ->width(300)
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    ],
    'name6',
    '1981-12',
    ReleaseDatePrecision::YEAR,
    'spotify:album:2up3OPMp9Tb4dAKM2erWXQ',
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
    ],
    PagingSimplifiedTrackObjectBuilder::init(
        'https://api.spotify.com/v1/me/shows?offset=0&limit=20
',
        20,
        0,
        4,
        [
            SimplifiedTrackObjectBuilder::init()
                ->artists(
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
                ->availableMarkets(
                    [
                        'available_markets2'
                    ]
                )
                ->discNumber(244)
                ->durationMs(52)
                ->explicit(false)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
        ->next('https://api.spotify.com/v1/me/shows?offset=1&limit=1')
        ->previous('https://api.spotify.com/v1/me/shows?offset=1&limit=1')
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build(),
    [
        CopyrightObjectBuilder::init()
            ->text('text2')
            ->type('type2')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    ],
    ExternalIdObjectBuilder::init()
        ->isrc('isrc8')
        ->ean('ean8')
        ->upc('upc2')
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build(),
    [
        'Egg punk',
        'Noise rock'
    ],
    'label6',
    152
)
    ->restrictions(
        AlbumRestrictionObjectBuilder::init()
            ->reason(Reason::EXPLICIT)
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



