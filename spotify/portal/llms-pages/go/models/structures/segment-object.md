# Segment Object

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/go/x-redirect/JTI0bSUyRlNlZ21lbnRPYmplY3Q

*This model accepts additional fields of type interface{}.*


# Class Name

`SegmentObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Start` | `*float64` | Optional | The starting point (in seconds) of the segment. |
| `Duration` | `*float64` | Optional | The duration (in seconds) of the segment. |
| `Confidence` | `*float64` | Optional | The confidence, from 0.0 to 1.0, of the reliability of the segmentation. Segments of the song which are difficult to logically segment (e.g: noise) may correspond to low values in this field.<br><br>**Constraints**: `>= 0`, `<= 1` |
| `LoudnessStart` | `*float64` | Optional | The onset loudness of the segment in decibels (dB). Combined with `loudness_max` and `loudness_max_time`, these components can be used to describe the "attack" of the segment. |
| `LoudnessMax` | `*float64` | Optional | The peak loudness of the segment in decibels (dB). Combined with `loudness_start` and `loudness_max_time`, these components can be used to describe the "attack" of the segment. |
| `LoudnessMaxTime` | `*float64` | Optional | The segment-relative offset of the segment peak loudness in seconds. Combined with `loudness_start` and `loudness_max`, these components can be used to desctibe the "attack" of the segment. |
| `LoudnessEnd` | `*float64` | Optional | The offset loudness of the segment in decibels (dB). This value should be equivalent to the loudness_start of the following segment. |
| `Pitches` | `[]float64` | Optional | Pitch content is given by a “chroma” vector, corresponding to the 12 pitch classes C, C#, D to B, with values ranging from 0 to 1 that describe the relative dominance of every pitch in the chromatic scale. For example a C Major chord would likely be represented by large values of C, E and G (i.e. classes 0, 4, and 7).<br><br>Vectors are normalized to 1 by their strongest dimension, therefore noisy sounds are likely represented by values that are all close to 1, while pure tones are described by one value at 1 (the pitch) and others near 0.<br>As can be seen below, the 12 vector indices are a combination of low-power spectrum values at their respective pitch frequencies.<br>![pitch vector](https://developer.spotify.com/assets/audio/Pitch_vector.png)<br><br>**Constraints**: `>= 0`, `<= 1` |
| `Timbre` | `[]float64` | Optional | Timbre is the quality of a musical note or sound that distinguishes different types of musical instruments, or voices. It is a complex notion also referred to as sound color, texture, or tone quality, and is derived from the shape of a segment’s spectro-temporal surface, independently of pitch and loudness. The timbre feature is a vector that includes 12 unbounded values roughly centered around 0. Those values are high level abstractions of the spectral surface, ordered by degree of importance.<br><br>For completeness however, the first dimension represents the average loudness of the segment; second emphasizes brightness; third is more closely correlated to the flatness of a sound; fourth to sounds with a stronger attack; etc. See an image below representing the 12 basis functions (i.e. template segments).<br>![timbre basis functions](https://developer.spotify.com/assets/audio/Timbre_basis_functions.png)<br><br>The actual timbre of the segment is best described as a linear combination of these 12 basis functions weighted by the coefficient values: timbre = c1 x b1 + c2 x b2 + ... + c12 x b12, where c1 to c12 represent the 12 coefficients and b1 to b12 the 12 basis functions as displayed below. Timbre vectors are best used in comparison with each other. |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    segmentObject := models.SegmentObject{
        Start:                 models.ToPointer(float64(0.70154)),
        Duration:              models.ToPointer(float64(0.19891)),
        Confidence:            models.ToPointer(float64(0.435)),
        LoudnessStart:         models.ToPointer(float64(-23.053)),
        LoudnessMax:           models.ToPointer(float64(-14.25)),
        LoudnessMaxTime:       models.ToPointer(float64(0.07305)),
        LoudnessEnd:           models.ToPointer(float64(0)),
        Pitches:               []float64{
            float64(0.212),
            float64(0.141),
            float64(0.294),
        },
        Timbre:                []float64{
            float64(42.115),
            float64(64.373),
            float64(-0.233),
        },
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



