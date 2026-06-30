# Me Tracks Request 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/net-standard-library/x-redirect/JTI0bSUyRk1lJTI1MjBUcmFja3MlMjUyMFJlcXVlc3Qx

*This model accepts additional fields of type object.*


# Class Name

`MeTracksRequest1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Ids` | `List<string>` | Optional | A JSON array of the [Spotify IDs](/documentation/web-api/concepts/spotify-uris-ids). For example: `["4iV5W9uYEdYUVa79Axb7Rh", "1301WleyT98MSxVHPZCA6M"]`<br/>A maximum of 50 items can be specified in one request. _**Note**: if the `ids` parameter is present in the query string, any IDs listed here in the body will be ignored._ |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models;
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Utilities;
using System.Collections.Generic;

MeTracksRequest1 meTracksRequest1 = new MeTracksRequest1
{
    Ids = new List<string>
    {
        "ids3",
        "ids4",
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



