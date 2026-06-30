# Track 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/net-standard-library/x-redirect/JTI0bSUyRlRyYWNrMQ

*This model accepts additional fields of type object.*


# Class Name

`Track1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Uri` | `string` | Optional | Spotify URI |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models;
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Utilities;

Track1 track1 = new Track1
{
    Uri = "uri0",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



