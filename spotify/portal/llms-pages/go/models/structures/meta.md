# Meta

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/go/x-redirect/JTI0bSUyRk1ldGE

*This model accepts additional fields of type interface{}.*


# Class Name

`Meta`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AnalyzerVersion` | `*string` | Optional | The version of the Analyzer used to analyze this track. |
| `Platform` | `*string` | Optional | The platform used to read the track's audio data. |
| `DetailedStatus` | `*string` | Optional | A detailed status code for this track. If analysis data is missing, this code may explain why. |
| `StatusCode` | `*int` | Optional | The return code of the analyzer process. 0 if successful, 1 if any errors occurred. |
| `Timestamp` | `*int64` | Optional | The Unix timestamp (in seconds) at which this track was analyzed. |
| `AnalysisTime` | `*float64` | Optional | The amount of time taken to analyze this track. |
| `InputProcess` | `*string` | Optional | The method used to read the track's audio data. |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    meta := models.Meta{
        AnalyzerVersion:       models.ToPointer("4.0.0"),
        Platform:              models.ToPointer("Linux"),
        DetailedStatus:        models.ToPointer("OK"),
        StatusCode:            models.ToPointer(0),
        Timestamp:             models.ToPointer(int64(1495193577)),
        AnalysisTime:          models.ToPointer(float64(6.93906)),
        InputProcess:          models.ToPointer("libvorbisfile L+R 44100->22050"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



