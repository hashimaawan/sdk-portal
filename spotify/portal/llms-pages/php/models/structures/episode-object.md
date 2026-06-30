# Episode Object

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/php/x-redirect/JTI0bSUyRkVwaXNvZGVPYmplY3Q

*This model accepts additional fields of type array.*


# Class Name

`EpisodeObject`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `audioPreviewUrl` | `?string` | Required | A URL to a 30 second preview (MP3 format) of the episode. `null` if not available. | getAudioPreviewUrl(): ?string | setAudioPreviewUrl(?string audioPreviewUrl): void |
| `description` | `string` | Required | A description of the episode. HTML tags are stripped away from this field, use `html_description` field in case HTML tags are needed. | getDescription(): string | setDescription(string description): void |
| `htmlDescription` | `string` | Required | A description of the episode. This field may contain HTML tags. | getHtmlDescription(): string | setHtmlDescription(string htmlDescription): void |
| `durationMs` | `int` | Required | The episode length in milliseconds. | getDurationMs(): int | setDurationMs(int durationMs): void |
| `explicit` | `bool` | Required | Whether or not the episode has explicit content (true = yes it does; false = no it does not OR unknown). | getExplicit(): bool | setExplicit(bool explicit): void |
| `externalUrls` | [`ExternalUrlObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/php/models/structures/external-url-object.md) | Required | External URLs for this episode. | getExternalUrls(): ExternalUrlObject | setExternalUrls(ExternalUrlObject externalUrls): void |
| `href` | `string` | Required | A link to the Web API endpoint providing full details of the episode. | getHref(): string | setHref(string href): void |
| `id` | `string` | Required | The [Spotify ID](/documentation/web-api/concepts/spotify-uris-ids) for the episode. | getId(): string | setId(string id): void |
| `images` | [`ImageObject[]`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/php/models/structures/image-object.md) | Required | The cover art for the episode in various sizes, widest first. | getImages(): array | setImages(array images): void |
| `isExternallyHosted` | `bool` | Required | True if the episode is hosted outside of Spotify's CDN. | getIsExternallyHosted(): bool | setIsExternallyHosted(bool isExternallyHosted): void |
| `isPlayable` | `bool` | Required | True if the episode is playable in the given market. Otherwise false. | getIsPlayable(): bool | setIsPlayable(bool isPlayable): void |
| `language` | `?string` | Optional | The language used in the episode, identified by a [ISO 639](https://en.wikipedia.org/wiki/ISO_639) code. This field is deprecated and might be removed in the future. Please use the `languages` field instead. | getLanguage(): ?string | setLanguage(?string language): void |
| `languages` | `string[]` | Required | A list of the languages used in the episode, identified by their [ISO 639-1](https://en.wikipedia.org/wiki/ISO_639) code. | getLanguages(): array | setLanguages(array languages): void |
| `name` | `string` | Required | The name of the episode. | getName(): string | setName(string name): void |
| `releaseDate` | `string` | Required | The date the episode was first released, for example `"1981-12-15"`. Depending on the precision, it might be shown as `"1981"` or `"1981-12"`. | getReleaseDate(): string | setReleaseDate(string releaseDate): void |
| `releaseDatePrecision` | [`string(ReleaseDatePrecision)`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/php/models/enumerations/release-date-precision.md) | Required | The precision with which `release_date` value is known. | getReleaseDatePrecision(): string | setReleaseDatePrecision(string releaseDatePrecision): void |
| `resumePoint` | [`?ResumePointObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/php/models/structures/resume-point-object.md) | Optional | The user's most recent position in the episode. Set if the supplied access token is a user token and has the scope 'user-read-playback-position'. | getResumePoint(): ?ResumePointObject | setResumePoint(?ResumePointObject resumePoint): void |
| `type` | `string` | Required, Constant | The object type.<br><br>**Value**: `'episode'` | getType(): string | setType(string type): void |
| `uri` | `string` | Required | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for the episode. | getUri(): string | setUri(string uri): void |
| `restrictions` | [`?EpisodeRestrictionObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/php/models/structures/episode-restriction-object.md) | Optional | Included in the response when a content restriction is applied. | getRestrictions(): ?EpisodeRestrictionObject | setRestrictions(?EpisodeRestrictionObject restrictions): void |
| `show` | [`ShowBase`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/php/models/structures/show-base.md) | Required | The show on which the episode belongs. | getShow(): ShowBase | setShow(ShowBase show): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\EpisodeObjectBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\ExternalUrlObjectBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\ApiHelper;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\ImageObjectBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\ReleaseDatePrecision;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\ShowBaseBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\CopyrightObjectBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\ResumePointObjectBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\EpisodeRestrictionObjectBuilder;

$episodeObject = EpisodeObjectBuilder::init(
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
    'spotify:episode:0zLhl3WsOCQHbe1BPTiHgr',
    ShowBaseBuilder::init(
        [
            'available_markets0',
            'available_markets1',
            'available_markets2'
        ],
        [
            CopyrightObjectBuilder::init()
                ->text('text2')
                ->type('type2')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ],
        'description4',
        'html_description4',
        false,
        ExternalUrlObjectBuilder::init()
            ->spotify('spotify6')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build(),
        'href8',
        'id6',
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
            'languages7',
            'languages6',
            'languages5'
        ],
        'media_type6',
        'name6',
        'publisher6',
        'uri0',
        198
    )
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build()
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
    ->build();
```



