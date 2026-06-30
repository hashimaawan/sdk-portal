# Playlists Request

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/go/x-redirect/JTI0bSUyRlBsYXlsaXN0cyUyNTIwUmVxdWVzdA

*This model accepts additional fields of type interface{}.*


# Class Name

`PlaylistsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Name` | `*string` | Optional | The new name for the playlist, for example `"My New Playlist Title"` |
| `Public` | `*bool` | Optional | If `true` the playlist will be public, if `false` it will be private. |
| `Collaborative` | `*bool` | Optional | If `true`, the playlist will become collaborative and other users will be able to modify the playlist in their Spotify client. <br/><br>_**Note**: You can only set `collaborative` to `true` on non-public playlists._ |
| `Description` | `*string` | Optional | Value for playlist description as displayed in Spotify Clients and in the Web API. |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    playlistsRequest := models.PlaylistsRequest{
        Name:                  models.ToPointer("Updated Playlist Name"),
        Public:                models.ToPointer(false),
        Collaborative:         models.ToPointer(false),
        Description:           models.ToPointer("Updated playlist description"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



