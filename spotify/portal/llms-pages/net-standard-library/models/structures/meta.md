# Meta

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/net-standard-library/x-redirect/JTI0bSUyRk1ldGE

*This model accepts additional fields of type object.*


# Class Name

`Meta`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AnalyzerVersion` | `string` | Optional | The version of the Analyzer used to analyze this track. |
| `Platform` | `string` | Optional | The platform used to read the track's audio data. |
| `DetailedStatus` | `string` | Optional | A detailed status code for this track. If analysis data is missing, this code may explain why. |
| `StatusCode` | `int?` | Optional | The return code of the analyzer process. 0 if successful, 1 if any errors occurred. |
| `Timestamp` | `long?` | Optional | The Unix timestamp (in seconds) at which this track was analyzed. |
| `AnalysisTime` | `double?` | Optional | The amount of time taken to analyze this track. |
| `InputProcess` | `string` | Optional | The method used to read the track's audio data. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models;
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Utilities;

Meta meta = new Meta
{
    AnalyzerVersion = "4.0.0",
    Platform = "Linux",
    DetailedStatus = "OK",
    StatusCode = 0,
    Timestamp = 1495193577L,
    AnalysisTime = 6.93906,
    InputProcess = "libvorbisfile L+R 44100->22050",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



