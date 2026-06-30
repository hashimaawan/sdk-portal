# Audio Analysis Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/go/x-redirect/JTI0bSUyRkF1ZGlvQW5hbHlzaXNPYmplY3Q

*This model accepts additional fields of type interface{}.*


# Class Name

`AudioAnalysisObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Meta` | [`*models.Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/go/models/structures/meta.md) | Optional | - |
| `Track` | [`*models.Track`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/go/models/structures/track.md) | Optional | - |
| `Bars` | [`[]models.TimeIntervalObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/go/models/structures/time-interval-object.md) | Optional | The time intervals of the bars throughout the track. A bar (or measure) is a segment of time defined as a given number of beats. |
| `Beats` | [`[]models.TimeIntervalObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/go/models/structures/time-interval-object.md) | Optional | The time intervals of beats throughout the track. A beat is the basic time unit of a piece of music; for example, each tick of a metronome. Beats are typically multiples of tatums. |
| `Sections` | [`[]models.SectionObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/go/models/structures/section-object.md) | Optional | Sections are defined by large variations in rhythm or timbre, e.g. chorus, verse, bridge, guitar solo, etc. Each section contains its own descriptions of tempo, key, mode, time_signature, and loudness. |
| `Segments` | [`[]models.SegmentObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/go/models/structures/segment-object.md) | Optional | Each segment contains a roughly conisistent sound throughout its duration. |
| `Tatums` | [`[]models.TimeIntervalObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/go/models/structures/time-interval-object.md) | Optional | A tatum represents the lowest regular pulse train that a listener intuitively infers from the timing of perceived musical events (segments). |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    audioAnalysisObject := models.AudioAnalysisObject{
        Meta:                  models.ToPointer(models.Meta{
            AnalyzerVersion:       models.ToPointer("analyzer_version8"),
            Platform:              models.ToPointer("platform6"),
            DetailedStatus:        models.ToPointer("detailed_status8"),
            StatusCode:            models.ToPointer(168),
            Timestamp:             models.ToPointer(int64(220)),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        Track:                 models.ToPointer(models.Track{
            NumSamples:              models.ToPointer(156),
            Duration:                models.ToPointer(float64(53.8)),
            SampleMd5:               models.ToPointer("sample_md56"),
            OffsetSeconds:           models.ToPointer(172),
            WindowSeconds:           models.ToPointer(42),
            AdditionalProperties:    map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        Bars:                  []models.TimeIntervalObject{
            models.TimeIntervalObject{
                Start:                 models.ToPointer(float64(141.7)),
                Duration:              models.ToPointer(float64(145.82)),
                Confidence:            models.ToPointer(float64(1)),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.TimeIntervalObject{
                Start:                 models.ToPointer(float64(141.7)),
                Duration:              models.ToPointer(float64(145.82)),
                Confidence:            models.ToPointer(float64(1)),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        Beats:                 []models.TimeIntervalObject{
            models.TimeIntervalObject{
                Start:                 models.ToPointer(float64(102.56)),
                Duration:              models.ToPointer(float64(106.68)),
                Confidence:            models.ToPointer(float64(1)),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.TimeIntervalObject{
                Start:                 models.ToPointer(float64(102.56)),
                Duration:              models.ToPointer(float64(106.68)),
                Confidence:            models.ToPointer(float64(1)),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.TimeIntervalObject{
                Start:                 models.ToPointer(float64(102.56)),
                Duration:              models.ToPointer(float64(106.68)),
                Confidence:            models.ToPointer(float64(1)),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        Sections:              []models.SectionObject{
            models.SectionObject{
                Start:                   models.ToPointer(float64(112.18)),
                Duration:                models.ToPointer(float64(116.3)),
                Confidence:              models.ToPointer(float64(1)),
                Loudness:                models.ToPointer(float64(14.46)),
                Tempo:                   models.ToPointer(float64(25)),
                AdditionalProperties:    map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.SectionObject{
                Start:                   models.ToPointer(float64(112.18)),
                Duration:                models.ToPointer(float64(116.3)),
                Confidence:              models.ToPointer(float64(1)),
                Loudness:                models.ToPointer(float64(14.46)),
                Tempo:                   models.ToPointer(float64(25)),
                AdditionalProperties:    map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



