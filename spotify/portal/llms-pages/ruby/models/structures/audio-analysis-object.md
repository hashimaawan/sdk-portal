# Audio Analysis Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/ruby/x-redirect/JTI0bSUyRkF1ZGlvQW5hbHlzaXNPYmplY3Q

*This model accepts additional fields of type Object.*


# Class Name

`AudioAnalysisObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/models/structures/meta.md) | Optional | - |
| `track` | [`Track`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/models/structures/track.md) | Optional | - |
| `bars` | [`Array[TimeIntervalObject]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/models/structures/time-interval-object.md) | Optional | The time intervals of the bars throughout the track. A bar (or measure) is a segment of time defined as a given number of beats. |
| `beats` | [`Array[TimeIntervalObject]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/models/structures/time-interval-object.md) | Optional | The time intervals of beats throughout the track. A beat is the basic time unit of a piece of music; for example, each tick of a metronome. Beats are typically multiples of tatums. |
| `sections` | [`Array[SectionObject]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/models/structures/section-object.md) | Optional | Sections are defined by large variations in rhythm or timbre, e.g. chorus, verse, bridge, guitar solo, etc. Each section contains its own descriptions of tempo, key, mode, time_signature, and loudness. |
| `segments` | [`Array[SegmentObject]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/models/structures/segment-object.md) | Optional | Each segment contains a roughly conisistent sound throughout its duration. |
| `tatums` | [`Array[TimeIntervalObject]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/models/structures/time-interval-object.md) | Optional | A tatum represents the lowest regular pulse train that a listener intuitively infers from the timing of perceived musical events (segments). |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
audio_analysis_object = AudioAnalysisObject.new(
  meta: Meta.new(
    analyzer_version: 'analyzer_version8',
    platform: 'platform6',
    detailed_status: 'detailed_status8',
    status_code: 168,
    timestamp: 220,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  track: Track.new(
    num_samples: 156,
    duration: 53.8,
    sample_md5: 'sample_md56',
    offset_seconds: 172,
    window_seconds: 42,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  bars: [
    TimeIntervalObject.new(
      start: 141.7,
      duration: 145.82,
      confidence: 1,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    TimeIntervalObject.new(
      start: 141.7,
      duration: 145.82,
      confidence: 1,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  beats: [
    TimeIntervalObject.new(
      start: 102.56,
      duration: 106.68,
      confidence: 1,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    TimeIntervalObject.new(
      start: 102.56,
      duration: 106.68,
      confidence: 1,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    TimeIntervalObject.new(
      start: 102.56,
      duration: 106.68,
      confidence: 1,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  sections: [
    SectionObject.new(
      start: 112.18,
      duration: 116.3,
      confidence: 1,
      loudness: 14.46,
      tempo: 25,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    SectionObject.new(
      start: 112.18,
      duration: 116.3,
      confidence: 1,
      loudness: 14.46,
      tempo: 25,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



