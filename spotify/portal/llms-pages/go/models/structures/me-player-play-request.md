# Me Player Play Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/go/x-redirect/JTI0bSUyRk1lJTI1MjBQbGF5ZXIlMjUyMFBsYXklMjUyMFJlcXVlc3Q

*This model accepts additional fields of type interface{}.*


# Class Name

`MePlayerPlayRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ContextUri` | `*string` | Optional | Optional. Spotify URI of the context to play.<br>Valid contexts are albums, artists & playlists.<br>`{context_uri:"spotify:album:1Je1IMUlBXcx1Fz0WE7oPT"}` |
| `Uris` | `[]string` | Optional | Optional. A JSON array of the Spotify track URIs to play.<br>For example: `{"uris": ["spotify:track:4iV5W9uYEdYUVa79Axb7Rh", "spotify:track:1301WleyT98MSxVHPZCA6M"]}` |
| `Offset` | `*interface{}` | Optional | Optional. Indicates from where in the context playback should start. Only available when context_uri corresponds to an album or playlist object<br>"position" is zero based and can’t be negative. Example: `"offset": {"position": 5}`<br>"uri" is a string representing the uri of the item to start at. Example: `"offset": {"uri": "spotify:track:1301WleyT98MSxVHPZCA6M"}` |
| `PositionMs` | `*int` | Optional | Indicates from what position to start playback. Must be a positive number. Passing in a position that is greater than the length of the track will cause the player to start playing the next song. |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    mePlayerPlayRequest := models.MePlayerPlayRequest{
        ContextUri:            models.ToPointer("spotify:album:5ht7ItJgpBH7W6vJ5BqpPr"),
        Uris:                  []string{
            "uris1",
        },
        Offset:                models.ToPointer(interface{}("[position, 5]")),
        PositionMs:            models.ToPointer(0),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



