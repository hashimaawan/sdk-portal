# Many Audio Features

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/typescript/x-redirect/JTI0bSUyRk1hbnlBdWRpb0ZlYXR1cmVz

*This model accepts additional fields of type unknown.*


# Interface Name

`ManyAudioFeatures`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `audioFeatures` | [`AudioFeaturesObject[]`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/typescript/models/structures/audio-features-object.md) | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  ManyAudioFeatures,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const manyAudioFeatures: ManyAudioFeatures = {
  audioFeatures: [
    {
      acousticness: 0.00242,
      analysisUrl: 'https://api.spotify.com/v1/audio-analysis/2takcwOaAZWiXQijPHIx7B\n',
      danceability: 0.585,
      durationMs: 237040,
      energy: 0.842,
      id: '2takcwOaAZWiXQijPHIx7B',
      instrumentalness: 0.00686,
      key: 9,
      liveness: 0.0866,
      loudness: -5.883,
      mode: 0,
      speechiness: 0.0556,
      tempo: 118.211,
      timeSignature: 4,
      trackHref: 'https://api.spotify.com/v1/tracks/2takcwOaAZWiXQijPHIx7B\n',
      uri: 'spotify:track:2takcwOaAZWiXQijPHIx7B',
      valence: 0.428,
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



