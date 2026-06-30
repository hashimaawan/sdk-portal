# Playlist Snapshot Id

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/go/x-redirect/JTI0bSUyRlBsYXlsaXN0U25hcHNob3RJZA

*This model accepts additional fields of type interface{}.*


# Class Name

`PlaylistSnapshotId`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `SnapshotId` | `*string` | Optional | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    playlistSnapshotId := models.PlaylistSnapshotId{
        SnapshotId:            models.ToPointer("abc"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



