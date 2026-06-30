# Playlist Tracks Ref Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/go/x-redirect/JTI0bSUyRlBsYXlsaXN0VHJhY2tzUmVmT2JqZWN0

*This model accepts additional fields of type interface{}.*


# Class Name

`PlaylistTracksRefObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Href` | `*string` | Optional | A link to the Web API endpoint where full details of the playlist's tracks can be retrieved. |
| `Total` | `*int` | Optional | Number of tracks in the playlist. |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    playlistTracksRefObject := models.PlaylistTracksRefObject{
        Href:                  models.ToPointer("href6"),
        Total:                 models.ToPointer(80),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



