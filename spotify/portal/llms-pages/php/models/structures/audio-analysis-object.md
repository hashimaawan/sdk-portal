# Audio Analysis Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/php/x-redirect/JTI0bSUyRkF1ZGlvQW5hbHlzaXNPYmplY3Q

*This model accepts additional fields of type array.*


# Class Name

`AudioAnalysisObject`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `meta` | [`?Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/php/models/structures/meta.md) | Optional | - | getMeta(): ?Meta | setMeta(?Meta meta): void |
| `track` | [`?Track`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/php/models/structures/track.md) | Optional | - | getTrack(): ?Track | setTrack(?Track track): void |
| `bars` | [`?(TimeIntervalObject[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/php/models/structures/time-interval-object.md) | Optional | The time intervals of the bars throughout the track. A bar (or measure) is a segment of time defined as a given number of beats. | getBars(): ?array | setBars(?array bars): void |
| `beats` | [`?(TimeIntervalObject[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/php/models/structures/time-interval-object.md) | Optional | The time intervals of beats throughout the track. A beat is the basic time unit of a piece of music; for example, each tick of a metronome. Beats are typically multiples of tatums. | getBeats(): ?array | setBeats(?array beats): void |
| `sections` | [`?(SectionObject[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/php/models/structures/section-object.md) | Optional | Sections are defined by large variations in rhythm or timbre, e.g. chorus, verse, bridge, guitar solo, etc. Each section contains its own descriptions of tempo, key, mode, time_signature, and loudness. | getSections(): ?array | setSections(?array sections): void |
| `segments` | [`?(SegmentObject[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/php/models/structures/segment-object.md) | Optional | Each segment contains a roughly conisistent sound throughout its duration. | getSegments(): ?array | setSegments(?array segments): void |
| `tatums` | [`?(TimeIntervalObject[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/php/models/structures/time-interval-object.md) | Optional | A tatum represents the lowest regular pulse train that a listener intuitively infers from the timing of perceived musical events (segments). | getTatums(): ?array | setTatums(?array tatums): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\AudioAnalysisObjectBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\MetaBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\ApiHelper;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\TrackBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\TimeIntervalObjectBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\SectionObjectBuilder;

$audioAnalysisObject = AudioAnalysisObjectBuilder::init()
    ->meta(
        MetaBuilder::init()
            ->analyzerVersion('analyzer_version8')
            ->platform('platform6')
            ->detailedStatus('detailed_status8')
            ->statusCode(168)
            ->timestamp(220)
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->track(
        TrackBuilder::init()
            ->numSamples(156)
            ->duration(53.8)
            ->sampleMd5('sample_md56')
            ->offsetSeconds(172)
            ->windowSeconds(42)
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->bars(
        [
            TimeIntervalObjectBuilder::init()
                ->start(141.7)
                ->duration(145.82)
                ->confidence(1)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            TimeIntervalObjectBuilder::init()
                ->start(141.7)
                ->duration(145.82)
                ->confidence(1)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->beats(
        [
            TimeIntervalObjectBuilder::init()
                ->start(102.56)
                ->duration(106.68)
                ->confidence(1)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            TimeIntervalObjectBuilder::init()
                ->start(102.56)
                ->duration(106.68)
                ->confidence(1)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            TimeIntervalObjectBuilder::init()
                ->start(102.56)
                ->duration(106.68)
                ->confidence(1)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->sections(
        [
            SectionObjectBuilder::init()
                ->start(112.18)
                ->duration(116.3)
                ->confidence(1)
                ->loudness(14.46)
                ->tempo(25)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            SectionObjectBuilder::init()
                ->start(112.18)
                ->duration(116.3)
                ->confidence(1)
                ->loudness(14.46)
                ->tempo(25)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



