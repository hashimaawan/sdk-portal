# Me Player Play Request

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/net-standard-library/x-redirect/JTI0bSUyRk1lJTI1MjBQbGF5ZXIlMjUyMFBsYXklMjUyMFJlcXVlc3Q

*This model accepts additional fields of type object.*


# Class Name

`MePlayerPlayRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ContextUri` | `string` | Optional | Optional. Spotify URI of the context to play.<br>Valid contexts are albums, artists & playlists.<br>`{context_uri:"spotify:album:1Je1IMUlBXcx1Fz0WE7oPT"}` |
| `Uris` | `List<string>` | Optional | Optional. A JSON array of the Spotify track URIs to play.<br>For example: `{"uris": ["spotify:track:4iV5W9uYEdYUVa79Axb7Rh", "spotify:track:1301WleyT98MSxVHPZCA6M"]}` |
| `Offset` | `object` | Optional | Optional. Indicates from where in the context playback should start. Only available when context_uri corresponds to an album or playlist object<br>"position" is zero based and can’t be negative. Example: `"offset": {"position": 5}`<br>"uri" is a string representing the uri of the item to start at. Example: `"offset": {"uri": "spotify:track:1301WleyT98MSxVHPZCA6M"}` |
| `PositionMs` | `int?` | Optional | Indicates from what position to start playback. Must be a positive number. Passing in a position that is greater than the length of the track will cause the player to start playing the next song. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models;
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Utilities;
using System.Collections.Generic;

MePlayerPlayRequest mePlayerPlayRequest = new MePlayerPlayRequest
{
    ContextUri = "spotify:album:5ht7ItJgpBH7W6vJ5BqpPr",
    Uris = new List<string>
    {
        "uris1",
    },
    Offset = ApiHelper.JsonDeserialize<object>("{\"position\":5}"),
    PositionMs = 0,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



