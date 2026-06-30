# Paged Albums

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/php/x-redirect/JTI0bSUyRlBhZ2VkQWxidW1z

*This model accepts additional fields of type array.*


# Class Name

`PagedAlbums`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `albums` | [`PagingSimplifiedAlbumObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/php/models/structures/paging-simplified-album-object.md) | Required | - | getAlbums(): PagingSimplifiedAlbumObject | setAlbums(PagingSimplifiedAlbumObject albums): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\PagedAlbumsBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\PagingSimplifiedAlbumObjectBuilder;
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

$pagedAlbums = PagedAlbumsBuilder::init(
    PagingSimplifiedAlbumObjectBuilder::init(
        'https://api.spotify.com/v1/me/shows?offset=0&limit=20
',
        20,
        0,
        4,
        [
            SimplifiedAlbumObjectBuilder::init(
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
                'href0',
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
                'name8',
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
        ->next('https://api.spotify.com/v1/me/shows?offset=1&limit=1')
        ->previous('https://api.spotify.com/v1/me/shows?offset=1&limit=1')
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build()
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



