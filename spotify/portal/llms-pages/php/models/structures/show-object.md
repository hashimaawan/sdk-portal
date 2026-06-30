# Show Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/php/x-redirect/JTI0bSUyRlNob3dPYmplY3Q

*This model accepts additional fields of type array.*


# Class Name

`ShowObject`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `availableMarkets` | `string[]` | Required | A list of the countries in which the show can be played, identified by their [ISO 3166-1 alpha-2](http://en.wikipedia.org/wiki/ISO_3166-1_alpha-2) code. | getAvailableMarkets(): array | setAvailableMarkets(array availableMarkets): void |
| `copyrights` | [`CopyrightObject[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/php/models/structures/copyright-object.md) | Required | The copyright statements of the show. | getCopyrights(): array | setCopyrights(array copyrights): void |
| `description` | `string` | Required | A description of the show. HTML tags are stripped away from this field, use `html_description` field in case HTML tags are needed. | getDescription(): string | setDescription(string description): void |
| `htmlDescription` | `string` | Required | A description of the show. This field may contain HTML tags. | getHtmlDescription(): string | setHtmlDescription(string htmlDescription): void |
| `explicit` | `bool` | Required | Whether or not the show has explicit content (true = yes it does; false = no it does not OR unknown). | getExplicit(): bool | setExplicit(bool explicit): void |
| `externalUrls` | [`ExternalUrlObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/php/models/structures/external-url-object.md) | Required | External URLs for this show. | getExternalUrls(): ExternalUrlObject | setExternalUrls(ExternalUrlObject externalUrls): void |
| `href` | `string` | Required | A link to the Web API endpoint providing full details of the show. | getHref(): string | setHref(string href): void |
| `id` | `string` | Required | The [Spotify ID](/documentation/web-api/concepts/spotify-uris-ids) for the show. | getId(): string | setId(string id): void |
| `images` | [`ImageObject[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/php/models/structures/image-object.md) | Required | The cover art for the show in various sizes, widest first. | getImages(): array | setImages(array images): void |
| `isExternallyHosted` | `bool` | Required | True if all of the shows episodes are hosted outside of Spotify's CDN. This field might be `null` in some cases. | getIsExternallyHosted(): bool | setIsExternallyHosted(bool isExternallyHosted): void |
| `languages` | `string[]` | Required | A list of the languages used in the show, identified by their [ISO 639](https://en.wikipedia.org/wiki/ISO_639) code. | getLanguages(): array | setLanguages(array languages): void |
| `mediaType` | `string` | Required | The media type of the show. | getMediaType(): string | setMediaType(string mediaType): void |
| `name` | `string` | Required | The name of the episode. | getName(): string | setName(string name): void |
| `publisher` | `string` | Required | The publisher of the show. | getPublisher(): string | setPublisher(string publisher): void |
| `type` | `string` | Required, Constant | The object type.<br><br>**Value**: `'show'` | getType(): string | setType(string type): void |
| `uri` | `string` | Required | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for the show. | getUri(): string | setUri(string uri): void |
| `totalEpisodes` | `int` | Required | The total number of episodes in the show. | getTotalEpisodes(): int | setTotalEpisodes(int totalEpisodes): void |
| `episodes` | [`PagingSimplifiedEpisodeObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/php/models/structures/paging-simplified-episode-object.md) | Required | The episodes of the show. | getEpisodes(): PagingSimplifiedEpisodeObject | setEpisodes(PagingSimplifiedEpisodeObject episodes): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\ShowObjectBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\CopyrightObjectBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\ApiHelper;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\ExternalUrlObjectBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\ImageObjectBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\PagingSimplifiedEpisodeObjectBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\EpisodeBaseBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\ReleaseDatePrecision;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\ResumePointObjectBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\EpisodeRestrictionObjectBuilder;

$showObject = ShowObjectBuilder::init(
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
    'description8',
    'html_description8',
    false,
    ExternalUrlObjectBuilder::init()
        ->spotify('spotify6')
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build(),
    'href0',
    'id8',
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
    false,
    [
        'languages5'
    ],
    'media_type6',
    'name8',
    'publisher6',
    'uri2',
    230,
    PagingSimplifiedEpisodeObjectBuilder::init(
        'https://api.spotify.com/v1/me/shows?offset=0&limit=20
',
        20,
        0,
        4,
        [
            EpisodeBaseBuilder::init(
                'A Spotify podcast sharing fresh insights on important topics of the moment—in a way only Spotify can. You’ll hear from experts in the music, podcast and tech industries as we discover and uncover stories about our work and the world around us.
',
                '<p>A Spotify podcast sharing fresh insights on important topics of the moment—in a way only Spotify can. You’ll hear from experts in the music, podcast and tech industries as we discover and uncover stories about our work and the world around us.</p>
',
                1686230,
                false,
                ExternalUrlObjectBuilder::init()
                    ->spotify('spotify6')
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build(),
                'https://api.spotify.com/v1/episodes/5Xt5DXGzch68nYYamXrNxZ',
                '5Xt5DXGzch68nYYamXrNxZ',
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
                false,
                false,
                [
                    'fr',
                    'en'
                ],
                'Starting Your Own Podcast: Tips, Tricks, and Advice From Anchor Creators
',
                '1981-12-15',
                ReleaseDatePrecision::DAY,
                'spotify:episode:0zLhl3WsOCQHbe1BPTiHgr'
            )
                ->audioPreviewUrl('https://p.scdn.co/mp3-preview/2f37da1d4221f40b9d1a98cd191f4d6f1646ad17')
                ->language('en')
                ->resumePoint(
                    ResumePointObjectBuilder::init()
                        ->fullyPlayed(false)
                        ->resumePositionMs(254)
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                )
                ->restrictions(
                    EpisodeRestrictionObjectBuilder::init()
                        ->reason('reason0')
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                )
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
        ->next('https://api.spotify.com/v1/me/shows?offset=1&limit=1')
        ->previous('https://api.spotify.com/v1/me/shows?offset=1&limit=1')
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build()
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



