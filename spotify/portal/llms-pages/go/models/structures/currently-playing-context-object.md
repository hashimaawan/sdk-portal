# Currently Playing Context Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/go/x-redirect/JTI0bSUyRkN1cnJlbnRseVBsYXlpbmdDb250ZXh0T2JqZWN0

*This model accepts additional fields of type interface{}.*


# Class Name

`CurrentlyPlayingContextObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Device` | [`*models.DeviceObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/go/models/structures/device-object.md) | Optional | The device that is currently active. |
| `RepeatState` | `*string` | Optional | off, track, context |
| `ShuffleState` | `*bool` | Optional | If shuffle is on or off. |
| `Context` | [`*models.ContextObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/go/models/structures/context-object.md) | Optional | A Context Object. Can be `null`. |
| `Timestamp` | `*int64` | Optional | Unix Millisecond Timestamp when data was fetched. |
| `ProgressMs` | `*int` | Optional | Progress into the currently playing track or episode. Can be `null`. |
| `IsPlaying` | `*bool` | Optional | If something is currently playing, return `true`. |
| `Item` | [`*models.CurrentlyPlayingContextObjectItem`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/go/models/oneof-anyof-definitions/currently-playing-context-object-item.md) | Optional | This is a container for one-of cases. |
| `CurrentlyPlayingType` | `*string` | Optional | The object type of the currently playing item. Can be one of `track`, `episode`, `ad` or `unknown`. |
| `Actions` | [`*models.DisallowsObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/go/models/structures/disallows-object.md) | Optional | Allows to update the user interface based on which playback actions are available within the current context. |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    currentlyPlayingContextObject := models.CurrentlyPlayingContextObject{
        Device:                models.ToPointer(models.DeviceObject{
            Id:                    models.NewOptional(models.ToPointer("id6")),
            IsActive:              models.ToPointer(false),
            IsPrivateSession:      models.ToPointer(false),
            IsRestricted:          models.ToPointer(false),
            Name:                  models.ToPointer("name6"),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        RepeatState:           models.ToPointer("repeat_state8"),
        ShuffleState:          models.ToPointer(false),
        Context:               models.ToPointer(models.ContextObject{
            Type:                  models.ToPointer("type8"),
            Href:                  models.ToPointer("href4"),
            ExternalUrls:          models.ToPointer(models.ExternalUrlObject{
                Spotify:               models.ToPointer("spotify6"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            }),
            Uri:                   models.ToPointer("uri6"),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        Timestamp:             models.ToPointer(int64(48)),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



