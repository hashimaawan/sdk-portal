# Audio Analysis Object

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/net-standard-library/x-redirect/JTI0bSUyRkF1ZGlvQW5hbHlzaXNPYmplY3Q

*This model accepts additional fields of type object.*


# Class Name

`AudioAnalysisObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Meta` | [`Meta`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/net-standard-library/models/structures/meta.md) | Optional | - |
| `Track` | [`Track`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/net-standard-library/models/structures/track.md) | Optional | - |
| `Bars` | [`List<TimeIntervalObject>`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/net-standard-library/models/structures/time-interval-object.md) | Optional | The time intervals of the bars throughout the track. A bar (or measure) is a segment of time defined as a given number of beats. |
| `Beats` | [`List<TimeIntervalObject>`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/net-standard-library/models/structures/time-interval-object.md) | Optional | The time intervals of beats throughout the track. A beat is the basic time unit of a piece of music; for example, each tick of a metronome. Beats are typically multiples of tatums. |
| `Sections` | [`List<SectionObject>`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/net-standard-library/models/structures/section-object.md) | Optional | Sections are defined by large variations in rhythm or timbre, e.g. chorus, verse, bridge, guitar solo, etc. Each section contains its own descriptions of tempo, key, mode, time_signature, and loudness. |
| `Segments` | [`List<SegmentObject>`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/net-standard-library/models/structures/segment-object.md) | Optional | Each segment contains a roughly conisistent sound throughout its duration. |
| `Tatums` | [`List<TimeIntervalObject>`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/net-standard-library/models/structures/time-interval-object.md) | Optional | A tatum represents the lowest regular pulse train that a listener intuitively infers from the timing of perceived musical events (segments). |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models;
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Utilities;
using System.Collections.Generic;

AudioAnalysisObject audioAnalysisObject = new AudioAnalysisObject
{
    Meta = new Meta
    {
        AnalyzerVersion = "analyzer_version8",
        Platform = "platform6",
        DetailedStatus = "detailed_status8",
        StatusCode = 168,
        Timestamp = 220L,
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    Track = new Track
    {
        NumSamples = 156,
        Duration = 53.8,
        SampleMd5 = "sample_md56",
        OffsetSeconds = 172,
        WindowSeconds = 42,
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    Bars = new List<TimeIntervalObject>
    {
        new TimeIntervalObject
        {
            Start = 141.7,
            Duration = 145.82,
            Confidence = 1,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new TimeIntervalObject
        {
            Start = 141.7,
            Duration = 145.82,
            Confidence = 1,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    Beats = new List<TimeIntervalObject>
    {
        new TimeIntervalObject
        {
            Start = 102.56,
            Duration = 106.68,
            Confidence = 1,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new TimeIntervalObject
        {
            Start = 102.56,
            Duration = 106.68,
            Confidence = 1,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new TimeIntervalObject
        {
            Start = 102.56,
            Duration = 106.68,
            Confidence = 1,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    Sections = new List<SectionObject>
    {
        new SectionObject
        {
            Start = 112.18,
            Duration = 116.3,
            Confidence = 1,
            Loudness = 14.46,
            Tempo = 25,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new SectionObject
        {
            Start = 112.18,
            Duration = 116.3,
            Confidence = 1,
            Loudness = 14.46,
            Tempo = 25,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



