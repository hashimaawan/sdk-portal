# Audio Analysis Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/typescript/x-redirect/JTI0bSUyRkF1ZGlvQW5hbHlzaXNPYmplY3Q

*This model accepts additional fields of type unknown.*


# Interface Name

`AudioAnalysisObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `meta` | [`Meta \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/typescript/models/structures/meta.md) | Optional | - |
| `track` | [`Track \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/typescript/models/structures/track.md) | Optional | - |
| `bars` | [`TimeIntervalObject[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/typescript/models/structures/time-interval-object.md) | Optional | The time intervals of the bars throughout the track. A bar (or measure) is a segment of time defined as a given number of beats. |
| `beats` | [`TimeIntervalObject[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/typescript/models/structures/time-interval-object.md) | Optional | The time intervals of beats throughout the track. A beat is the basic time unit of a piece of music; for example, each tick of a metronome. Beats are typically multiples of tatums. |
| `sections` | [`SectionObject[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/typescript/models/structures/section-object.md) | Optional | Sections are defined by large variations in rhythm or timbre, e.g. chorus, verse, bridge, guitar solo, etc. Each section contains its own descriptions of tempo, key, mode, time_signature, and loudness. |
| `segments` | [`SegmentObject[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/typescript/models/structures/segment-object.md) | Optional | Each segment contains a roughly conisistent sound throughout its duration. |
| `tatums` | [`TimeIntervalObject[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/typescript/models/structures/time-interval-object.md) | Optional | A tatum represents the lowest regular pulse train that a listener intuitively infers from the timing of perceived musical events (segments). |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  AudioAnalysisObject,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const audioAnalysisObject: AudioAnalysisObject = {
  meta: {
    analyzerVersion: 'analyzer_version8',
    platform: 'platform6',
    detailedStatus: 'detailed_status8',
    statusCode: 168,
    timestamp: BigInt(220),
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  track: {
    numSamples: 156,
    duration: 53.8,
    sampleMd5: 'sample_md56',
    offsetSeconds: 172,
    windowSeconds: 42,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  bars: [
    {
      start: 141.7,
      duration: 145.82,
      confidence: 1,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      start: 141.7,
      duration: 145.82,
      confidence: 1,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  beats: [
    {
      start: 102.56,
      duration: 106.68,
      confidence: 1,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      start: 102.56,
      duration: 106.68,
      confidence: 1,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      start: 102.56,
      duration: 106.68,
      confidence: 1,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  sections: [
    {
      start: 112.18,
      duration: 116.3,
      confidence: 1,
      loudness: 14.46,
      tempo: 25,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      start: 112.18,
      duration: 116.3,
      confidence: 1,
      loudness: 14.46,
      tempo: 25,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



