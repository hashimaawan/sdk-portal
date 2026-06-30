# Resume Point Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/net-standard-library/x-redirect/JTI0bSUyRlJlc3VtZVBvaW50T2JqZWN0

*This model accepts additional fields of type object.*


# Class Name

`ResumePointObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `FullyPlayed` | `bool?` | Optional | Whether or not the episode has been fully played by the user. |
| `ResumePositionMs` | `int?` | Optional | The user's most recent position in the episode in milliseconds. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models;
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Utilities;

ResumePointObject resumePointObject = new ResumePointObject
{
    FullyPlayed = false,
    ResumePositionMs = 106,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



