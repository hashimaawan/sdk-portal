# Audio Features Object

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/net-standard-library/x-redirect/JTI0bSUyRkF1ZGlvRmVhdHVyZXNPYmplY3Q

*This model accepts additional fields of type object.*


# Class Name

`AudioFeaturesObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Acousticness` | `double?` | Optional | A confidence measure from 0.0 to 1.0 of whether the track is acoustic. 1.0 represents high confidence the track is acoustic.<br><br>**Constraints**: `>= 0`, `<= 1` |
| `AnalysisUrl` | `string` | Optional | A URL to access the full audio analysis of this track. An access token is required to access this data. |
| `Danceability` | `double?` | Optional | Danceability describes how suitable a track is for dancing based on a combination of musical elements including tempo, rhythm stability, beat strength, and overall regularity. A value of 0.0 is least danceable and 1.0 is most danceable. |
| `DurationMs` | `int?` | Optional | The duration of the track in milliseconds. |
| `Energy` | `double?` | Optional | Energy is a measure from 0.0 to 1.0 and represents a perceptual measure of intensity and activity. Typically, energetic tracks feel fast, loud, and noisy. For example, death metal has high energy, while a Bach prelude scores low on the scale. Perceptual features contributing to this attribute include dynamic range, perceived loudness, timbre, onset rate, and general entropy. |
| `Id` | `string` | Optional | The Spotify ID for the track. |
| `Instrumentalness` | `double?` | Optional | Predicts whether a track contains no vocals. "Ooh" and "aah" sounds are treated as instrumental in this context. Rap or spoken word tracks are clearly "vocal". The closer the instrumentalness value is to 1.0, the greater likelihood the track contains no vocal content. Values above 0.5 are intended to represent instrumental tracks, but confidence is higher as the value approaches 1.0. |
| `Key` | `int?` | Optional | The key the track is in. Integers map to pitches using standard [Pitch Class notation](https://en.wikipedia.org/wiki/Pitch_class). E.g. 0 = C, 1 = C♯/D♭, 2 = D, and so on. If no key was detected, the value is -1.<br><br>**Constraints**: `>= -1`, `<= 11` |
| `Liveness` | `double?` | Optional | Detects the presence of an audience in the recording. Higher liveness values represent an increased probability that the track was performed live. A value above 0.8 provides strong likelihood that the track is live. |
| `Loudness` | `double?` | Optional | The overall loudness of a track in decibels (dB). Loudness values are averaged across the entire track and are useful for comparing relative loudness of tracks. Loudness is the quality of a sound that is the primary psychological correlate of physical strength (amplitude). Values typically range between -60 and 0 db. |
| `Mode` | `int?` | Optional | Mode indicates the modality (major or minor) of a track, the type of scale from which its melodic content is derived. Major is represented by 1 and minor is 0. |
| `Speechiness` | `double?` | Optional | Speechiness detects the presence of spoken words in a track. The more exclusively speech-like the recording (e.g. talk show, audio book, poetry), the closer to 1.0 the attribute value. Values above 0.66 describe tracks that are probably made entirely of spoken words. Values between 0.33 and 0.66 describe tracks that may contain both music and speech, either in sections or layered, including such cases as rap music. Values below 0.33 most likely represent music and other non-speech-like tracks. |
| `Tempo` | `double?` | Optional | The overall estimated tempo of a track in beats per minute (BPM). In musical terminology, tempo is the speed or pace of a given piece and derives directly from the average beat duration. |
| `TimeSignature` | `int?` | Optional | An estimated time signature. The time signature (meter) is a notational convention to specify how many beats are in each bar (or measure). The time signature ranges from 3 to 7 indicating time signatures of "3/4", to "7/4".<br><br>**Constraints**: `>= 3`, `<= 7` |
| `TrackHref` | `string` | Optional | A link to the Web API endpoint providing full details of the track. |
| `Type` | [`Type5?`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/net-standard-library/models/enumerations/type-5.md) | Optional | The object type. |
| `Uri` | `string` | Optional | The Spotify URI for the track. |
| `Valence` | `double?` | Optional | A measure from 0.0 to 1.0 describing the musical positiveness conveyed by a track. Tracks with high valence sound more positive (e.g. happy, cheerful, euphoric), while tracks with low valence sound more negative (e.g. sad, depressed, angry).<br><br>**Constraints**: `>= 0`, `<= 1` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models;
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Utilities;

AudioFeaturesObject audioFeaturesObject = new AudioFeaturesObject
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
};
```



