# Currently Playing Context Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/net-standard-library/x-redirect/JTI0bSUyRkN1cnJlbnRseVBsYXlpbmdDb250ZXh0T2JqZWN0

*This model accepts additional fields of type object.*


# Class Name

`CurrentlyPlayingContextObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Device` | [`DeviceObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/net-standard-library/models/structures/device-object.md) | Optional | The device that is currently active. |
| `RepeatState` | `string` | Optional | off, track, context |
| `ShuffleState` | `bool?` | Optional | If shuffle is on or off. |
| `Context` | [`ContextObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/net-standard-library/models/structures/context-object.md) | Optional | A Context Object. Can be `null`. |
| `Timestamp` | `long?` | Optional | Unix Millisecond Timestamp when data was fetched. |
| `ProgressMs` | `int?` | Optional | Progress into the currently playing track or episode. Can be `null`. |
| `IsPlaying` | `bool?` | Optional | If something is currently playing, return `true`. |
| `Item` | [`CurrentlyPlayingContextObjectItem`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/net-standard-library/models/oneof-anyof-definitions/currently-playing-context-object-item.md) | Optional | This is a container for one-of cases. |
| `CurrentlyPlayingType` | `string` | Optional | The object type of the currently playing item. Can be one of `track`, `episode`, `ad` or `unknown`. |
| `Actions` | [`DisallowsObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/net-standard-library/models/structures/disallows-object.md) | Optional | Allows to update the user interface based on which playback actions are available within the current context. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models;
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Utilities;

CurrentlyPlayingContextObject currentlyPlayingContextObject = new CurrentlyPlayingContextObject
{
    Device = new DeviceObject
    {
        Id = "id6",
        IsActive = false,
        IsPrivateSession = false,
        IsRestricted = false,
        Name = "name6",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    RepeatState = "repeat_state8",
    ShuffleState = false,
    Context = new ContextObject
    {
        Type = "type8",
        Href = "href4",
        ExternalUrls = new ExternalUrlObject
        {
            Spotify = "spotify6",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        Uri = "uri6",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    Timestamp = 48L,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



