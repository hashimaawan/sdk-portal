# Many Audio Features

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/php/x-redirect/JTI0bSUyRk1hbnlBdWRpb0ZlYXR1cmVz

*This model accepts additional fields of type array.*


# Class Name

`ManyAudioFeatures`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `audioFeatures` | [`AudioFeaturesObject[]`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/php/models/structures/audio-features-object.md) | Required | - | getAudioFeatures(): array | setAudioFeatures(array audioFeatures): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\ManyAudioFeaturesBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\AudioFeaturesObjectBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\ApiHelper;

$manyAudioFeatures = ManyAudioFeaturesBuilder::init(
    [
        AudioFeaturesObjectBuilder::init()
            ->acousticness(0.00242)
            ->analysisUrl('https://api.spotify.com/v1/audio-analysis/2takcwOaAZWiXQijPHIx7B
')
            ->danceability(0.585)
            ->durationMs(237040)
            ->energy(0.842)
            ->id('2takcwOaAZWiXQijPHIx7B')
            ->instrumentalness(0.00686)
            ->key(9)
            ->liveness(0.0866)
            ->loudness(-5.883)
            ->mode(0)
            ->speechiness(0.0556)
            ->tempo(118.211)
            ->timeSignature(4)
            ->trackHref('https://api.spotify.com/v1/tracks/2takcwOaAZWiXQijPHIx7B
')
            ->uri('spotify:track:2takcwOaAZWiXQijPHIx7B')
            ->valence(0.428)
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    ]
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



