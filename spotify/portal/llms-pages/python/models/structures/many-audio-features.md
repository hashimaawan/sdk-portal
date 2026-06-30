# Many Audio Features

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/python/x-redirect/JTI0bSUyRk1hbnlBdWRpb0ZlYXR1cmVz

*This model accepts additional fields of type Any.*


# Class Name

`ManyAudioFeatures`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `audio_features` | [`List[AudioFeaturesObject]`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/python/models/structures/audio-features-object.md) | Required | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from spotifywebapiwithfixesandimprovementsfromsonallux.models.audio_features_object import AudioFeaturesObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.many_audio_features import ManyAudioFeatures

many_audio_features = ManyAudioFeatures(
    audio_features=[
        AudioFeaturesObject(
            acousticness=0.00242,
            analysis_url='https://api.spotify.com/v1/audio-analysis/2takcwOaAZWiXQijPHIx7B\n',
            danceability=0.585,
            duration_ms=237040,
            energy=0.842,
            id='2takcwOaAZWiXQijPHIx7B',
            instrumentalness=0.00686,
            key=9,
            liveness=0.0866,
            loudness=-5.883,
            mode=0,
            speechiness=0.0556,
            tempo=118.211,
            time_signature=4,
            track_href='https://api.spotify.com/v1/tracks/2takcwOaAZWiXQijPHIx7B\n',
            uri='spotify:track:2takcwOaAZWiXQijPHIx7B',
            valence=0.428,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



