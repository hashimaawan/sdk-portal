# Saved Audiobook Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/php/x-redirect/JTI0bSUyRlNhdmVkQXVkaW9ib29rT2JqZWN0

*This model accepts additional fields of type array.*


# Class Name

`SavedAudiobookObject`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `addedAt` | `?DateTime` | Optional | The date and time the audiobook was saved<br>Timestamps are returned in ISO 8601 format as Coordinated Universal Time (UTC) with a zero offset: YYYY-MM-DDTHH:MM:SSZ.<br>If the time is imprecise (for example, the date/time of an album release), an additional field indicates the precision; see for example, release_date in an album object. | getAddedAt(): ?\DateTime | setAddedAt(?\DateTime addedAt): void |
| `audiobook` | [`?AudiobookObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/php/models/structures/audiobook-object.md) | Optional | Information about the audiobook. | getAudiobook(): ?AudiobookObject | setAudiobook(?AudiobookObject audiobook): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\SavedAudiobookObjectBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Utils\DateTimeHelper;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\AudiobookObjectBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\AuthorObjectBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\ApiHelper;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\CopyrightObjectBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\ExternalUrlObjectBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\ImageObjectBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\NarratorObjectBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\PagingSimplifiedChapterObjectBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\ChapterBaseBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\ReleaseDatePrecision;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\ResumePointObjectBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\ChapterRestrictionObjectBuilder;

$savedAudiobookObject = SavedAudiobookObjectBuilder::init()
    ->addedAt(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
    ->audiobook(
        AudiobookObjectBuilder::init(
            [
                AuthorObjectBuilder::init()
                    ->name('name0')
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            ],
            [
                'available_markets2',
                'available_markets3',
                'available_markets4'
            ],
            [
                CopyrightObjectBuilder::init()
                    ->text('text2')
                    ->type('type2')
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build(),
                CopyrightObjectBuilder::init()
                    ->text('text2')
                    ->type('type2')
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build(),
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
                    ->build(),
                ImageObjectBuilder::init(
                    'url6'
                )
                    ->height(182)
                    ->width(222)
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            ],
            [
                'languages3',
                'languages4'
            ],
            'media_type4',
            'name8',
            [
                NarratorObjectBuilder::init()
                    ->name('name0')
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build(),
                NarratorObjectBuilder::init()
                    ->name('name0')
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            ],
            'publisher4',
            'uri2',
            186,
            PagingSimplifiedChapterObjectBuilder::init(
                'href4',
                230,
                122,
                136,
                [
                    ChapterBaseBuilder::init(
                        164,
                        'description2',
                        'html_description2',
                        52,
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
                        'name8',
                        'release_date6',
                        ReleaseDatePrecision::MONTH,
                        'uri2'
                    )
                        ->audioPreviewUrl('audio_preview_url4')
                        ->availableMarkets(
                            [
                                'available_markets2'
                            ]
                        )
                        ->resumePoint(
                            ResumePointObjectBuilder::init()
                                ->fullyPlayed(false)
                                ->resumePositionMs(254)
                                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                ->build()
                        )
                        ->restrictions(
                            ChapterRestrictionObjectBuilder::init()
                                ->reason('reason0')
                                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                ->build()
                        )
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                ]
            )
                ->next('next0')
                ->previous('previous0')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        )
            ->edition('edition8')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



