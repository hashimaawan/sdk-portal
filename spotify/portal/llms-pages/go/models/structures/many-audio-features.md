# Many Audio Features

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/go/x-redirect/JTI0bSUyRk1hbnlBdWRpb0ZlYXR1cmVz

*This model accepts additional fields of type interface{}.*


# Class Name

`ManyAudioFeatures`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AudioFeatures` | [`[]models.AudioFeaturesObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/go/models/structures/audio-features-object.md) | Required | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    manyAudioFeatures := models.ManyAudioFeatures{
        AudioFeatures:         []models.AudioFeaturesObject{
            models.AudioFeaturesObject{
                Acousticness:          models.ToPointer(float64(0.00242)),
                AnalysisUrl:           models.ToPointer("https://api.spotify.com/v1/audio-analysis/2takcwOaAZWiXQijPHIx7B\n"),
                Danceability:          models.ToPointer(float64(0.585)),
                DurationMs:            models.ToPointer(237040),
                Energy:                models.ToPointer(float64(0.842)),
                Id:                    models.ToPointer("2takcwOaAZWiXQijPHIx7B"),
                Instrumentalness:      models.ToPointer(float64(0.00686)),
                Key:                   models.ToPointer(9),
                Liveness:              models.ToPointer(float64(0.0866)),
                Loudness:              models.ToPointer(float64(-5.883)),
                Mode:                  models.ToPointer(0),
                Speechiness:           models.ToPointer(float64(0.0556)),
                Tempo:                 models.ToPointer(float64(118.211)),
                TimeSignature:         models.ToPointer(4),
                TrackHref:             models.ToPointer("https://api.spotify.com/v1/tracks/2takcwOaAZWiXQijPHIx7B\n"),
                Uri:                   models.ToPointer("spotify:track:2takcwOaAZWiXQijPHIx7B"),
                Valence:               models.ToPointer(float64(0.428)),
                AdditionalProperties:  map[string]interface{}{
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



