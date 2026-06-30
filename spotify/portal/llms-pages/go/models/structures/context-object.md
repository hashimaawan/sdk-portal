# Context Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/go/x-redirect/JTI0bSUyRkNvbnRleHRPYmplY3Q

*This model accepts additional fields of type interface{}.*


# Class Name

`ContextObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Type` | `*string` | Optional | The object type, e.g. "artist", "playlist", "album", "show". |
| `Href` | `*string` | Optional | A link to the Web API endpoint providing full details of the track. |
| `ExternalUrls` | [`*models.ExternalUrlObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/go/models/structures/external-url-object.md) | Optional | External URLs for this context. |
| `Uri` | `*string` | Optional | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for the context. |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    contextObject := models.ContextObject{
        Type:                  models.ToPointer("type6"),
        Href:                  models.ToPointer("href6"),
        ExternalUrls:          models.ToPointer(models.ExternalUrlObject{
            Spotify:               models.ToPointer("spotify6"),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        Uri:                   models.ToPointer("uri8"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



