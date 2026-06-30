# Linked Track Object

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/go/x-redirect/JTI0bSUyRkxpbmtlZFRyYWNrT2JqZWN0

*This model accepts additional fields of type interface{}.*


# Class Name

`LinkedTrackObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ExternalUrls` | [`*models.ExternalUrlObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/go/models/structures/external-url-object.md) | Optional | Known external URLs for this track. |
| `Href` | `*string` | Optional | A link to the Web API endpoint providing full details of the track. |
| `Id` | `*string` | Optional | The [Spotify ID](/documentation/web-api/concepts/spotify-uris-ids) for the track. |
| `Type` | `*string` | Optional | The object type: "track". |
| `Uri` | `*string` | Optional | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for the track. |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    linkedTrackObject := models.LinkedTrackObject{
        ExternalUrls:          models.ToPointer(models.ExternalUrlObject{
            Spotify:               models.ToPointer("spotify6"),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        Href:                  models.ToPointer("href0"),
        Id:                    models.ToPointer("id8"),
        Type:                  models.ToPointer("type2"),
        Uri:                   models.ToPointer("uri2"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



