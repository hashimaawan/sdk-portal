# Many Audio Features

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/net-standard-library/x-redirect/JTI0bSUyRk1hbnlBdWRpb0ZlYXR1cmVz

*This model accepts additional fields of type object.*


# Class Name

`ManyAudioFeatures`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AudioFeatures` | [`List<AudioFeaturesObject>`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/net-standard-library/models/structures/audio-features-object.md) | Required | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models;
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Utilities;
using System.Collections.Generic;

ManyAudioFeatures manyAudioFeatures = new ManyAudioFeatures
{
    AudioFeatures = new List<AudioFeaturesObject>
    {
        new AudioFeaturesObject
        {
            Acousticness = 0.00242,
            AnalysisUrl = "https://api.spotify.com/v1/audio-analysis/2takcwOaAZWiXQijPHIx7B\n",
            Danceability = 0.585,
            DurationMs = 237040,
            Energy = 0.842,
            Id = "2takcwOaAZWiXQijPHIx7B",
            Instrumentalness = 0.00686,
            Key = 9,
            Liveness = 0.0866,
            Loudness = -5.883,
            Mode = 0,
            Speechiness = 0.0556,
            Tempo = 118.211,
            TimeSignature = 4,
            TrackHref = "https://api.spotify.com/v1/tracks/2takcwOaAZWiXQijPHIx7B\n",
            Uri = "spotify:track:2takcwOaAZWiXQijPHIx7B",
            Valence = 0.428,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



