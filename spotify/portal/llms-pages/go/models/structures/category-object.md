# Category Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/go/x-redirect/JTI0bSUyRkNhdGVnb3J5T2JqZWN0

*This model accepts additional fields of type interface{}.*


# Class Name

`CategoryObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Href` | `string` | Required | A link to the Web API endpoint returning full details of the category. |
| `Icons` | [`[]models.ImageObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/go/models/structures/image-object.md) | Required | The category icon, in various sizes. |
| `Id` | `string` | Required | The [Spotify category ID](/documentation/web-api/concepts/spotify-uris-ids) of the category. |
| `Name` | `string` | Required | The name of the category. |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    categoryObject := models.CategoryObject{
        Href:                  "href2",
        Icons:                 []models.ImageObject{
            models.ImageObject{
                Url:                   "https://i.scdn.co/image/ab67616d00001e02ff9ca10b55ce82ae553c8228\n",
                Height:                models.ToPointer(300),
                Width:                 models.ToPointer(300),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        Id:                    "equal",
        Name:                  "EQUAL",
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



