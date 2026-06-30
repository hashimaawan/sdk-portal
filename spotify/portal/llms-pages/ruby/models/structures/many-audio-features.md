# Many Audio Features

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/ruby/x-redirect/JTI0bSUyRk1hbnlBdWRpb0ZlYXR1cmVz

*This model accepts additional fields of type Object.*


# Class Name

`ManyAudioFeatures`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `audio_features` | [`Array[AudioFeaturesObject]`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/ruby/models/structures/audio-features-object.md) | Required | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
many_audio_features = ManyAudioFeatures.new(
  audio_features: [
    AudioFeaturesObject.new(
      acousticness: 0.00242,
      analysis_url: 'https://api.spotify.com/v1/audio-analysis/2takcwOaAZWiXQijPHIx7B\n',
      danceability: 0.585,
      duration_ms: 237040,
      energy: 0.842,
      id: '2takcwOaAZWiXQijPHIx7B',
      instrumentalness: 0.00686,
      key: 9,
      liveness: 0.0866,
      loudness: -5.883,
      mode: 0,
      speechiness: 0.0556,
      tempo: 118.211,
      time_signature: 4,
      track_href: 'https://api.spotify.com/v1/tracks/2takcwOaAZWiXQijPHIx7B\n',
      uri: 'spotify:track:2takcwOaAZWiXQijPHIx7B',
      valence: 0.428,
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



