# Track

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/go/x-redirect/JTI0bSUyRlRyYWNr

*This model accepts additional fields of type interface{}.*


# Class Name

`Track`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `NumSamples` | `*int` | Optional | The exact number of audio samples analyzed from this track. See also `analysis_sample_rate`. |
| `Duration` | `*float64` | Optional | Length of the track in seconds. |
| `SampleMd5` | `*string` | Optional | This field will always contain the empty string. |
| `OffsetSeconds` | `*int` | Optional | An offset to the start of the region of the track that was analyzed. (As the entire track is analyzed, this should always be 0.) |
| `WindowSeconds` | `*int` | Optional | The length of the region of the track was analyzed, if a subset of the track was analyzed. (As the entire track is analyzed, this should always be 0.) |
| `AnalysisSampleRate` | `*int` | Optional | The sample rate used to decode and analyze this track. May differ from the actual sample rate of this track available on Spotify. |
| `AnalysisChannels` | `*int` | Optional | The number of channels used for analysis. If 1, all channels are summed together to mono before analysis. |
| `EndOfFadeIn` | `*float64` | Optional | The time, in seconds, at which the track's fade-in period ends. If the track has no fade-in, this will be 0.0. |
| `StartOfFadeOut` | `*float64` | Optional | The time, in seconds, at which the track's fade-out period starts. If the track has no fade-out, this should match the track's length. |
| `Loudness` | `*float64` | Optional | The overall loudness of a track in decibels (dB). Loudness values are averaged across the entire track and are useful for comparing relative loudness of tracks. Loudness is the quality of a sound that is the primary psychological correlate of physical strength (amplitude). Values typically range between -60 and 0 db. |
| `Tempo` | `*float64` | Optional | The overall estimated tempo of a track in beats per minute (BPM). In musical terminology, tempo is the speed or pace of a given piece and derives directly from the average beat duration. |
| `TempoConfidence` | `*float64` | Optional | The confidence, from 0.0 to 1.0, of the reliability of the `tempo`.<br><br>**Constraints**: `>= 0`, `<= 1` |
| `TimeSignature` | `*int` | Optional | An estimated time signature. The time signature (meter) is a notational convention to specify how many beats are in each bar (or measure). The time signature ranges from 3 to 7 indicating time signatures of "3/4", to "7/4".<br><br>**Constraints**: `>= 3`, `<= 7` |
| `TimeSignatureConfidence` | `*float64` | Optional | The confidence, from 0.0 to 1.0, of the reliability of the `time_signature`.<br><br>**Constraints**: `>= 0`, `<= 1` |
| `Key` | `*int` | Optional | The key the track is in. Integers map to pitches using standard [Pitch Class notation](https://en.wikipedia.org/wiki/Pitch_class). E.g. 0 = C, 1 = C♯/D♭, 2 = D, and so on. If no key was detected, the value is -1.<br><br>**Constraints**: `>= -1`, `<= 11` |
| `KeyConfidence` | `*float64` | Optional | The confidence, from 0.0 to 1.0, of the reliability of the `key`.<br><br>**Constraints**: `>= 0`, `<= 1` |
| `Mode` | `*int` | Optional | Mode indicates the modality (major or minor) of a track, the type of scale from which its melodic content is derived. Major is represented by 1 and minor is 0. |
| `ModeConfidence` | `*float64` | Optional | The confidence, from 0.0 to 1.0, of the reliability of the `mode`.<br><br>**Constraints**: `>= 0`, `<= 1` |
| `Codestring` | `*string` | Optional | An [Echo Nest Musical Fingerprint (ENMFP)](https://academiccommons.columbia.edu/doi/10.7916/D8Q248M4) codestring for this track. |
| `CodeVersion` | `*float64` | Optional | A version number for the Echo Nest Musical Fingerprint format used in the codestring field. |
| `Echoprintstring` | `*string` | Optional | An [EchoPrint](https://github.com/spotify/echoprint-codegen) codestring for this track. |
| `EchoprintVersion` | `*float64` | Optional | A version number for the EchoPrint format used in the echoprintstring field. |
| `Synchstring` | `*string` | Optional | A [Synchstring](https://github.com/echonest/synchdata) for this track. |
| `SynchVersion` | `*float64` | Optional | A version number for the Synchstring used in the synchstring field. |
| `Rhythmstring` | `*string` | Optional | A Rhythmstring for this track. The format of this string is similar to the Synchstring. |
| `RhythmVersion` | `*float64` | Optional | A version number for the Rhythmstring used in the rhythmstring field. |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    track := models.Track{
        NumSamples:              models.ToPointer(4585515),
        Duration:                models.ToPointer(float64(207.95985)),
        SampleMd5:               models.ToPointer("sample_md56"),
        OffsetSeconds:           models.ToPointer(0),
        WindowSeconds:           models.ToPointer(0),
        AnalysisSampleRate:      models.ToPointer(22050),
        AnalysisChannels:        models.ToPointer(1),
        EndOfFadeIn:             models.ToPointer(float64(0)),
        StartOfFadeOut:          models.ToPointer(float64(201.13705)),
        Loudness:                models.ToPointer(float64(-5.883)),
        Tempo:                   models.ToPointer(float64(118.211)),
        TempoConfidence:         models.ToPointer(float64(0.73)),
        TimeSignature:           models.ToPointer(4),
        TimeSignatureConfidence: models.ToPointer(float64(0.994)),
        Key:                     models.ToPointer(9),
        KeyConfidence:           models.ToPointer(float64(0.408)),
        Mode:                    models.ToPointer(0),
        ModeConfidence:          models.ToPointer(float64(0.485)),
        CodeVersion:             models.ToPointer(float64(3.15)),
        EchoprintVersion:        models.ToPointer(float64(4.15)),
        SynchVersion:            models.ToPointer(float64(1)),
        RhythmVersion:           models.ToPointer(float64(1)),
        AdditionalProperties:    map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



