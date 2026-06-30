# Paged Categories

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/go/x-redirect/JTI0bSUyRlBhZ2VkQ2F0ZWdvcmllcw

*This model accepts additional fields of type interface{}.*


# Class Name

`PagedCategories`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Categories` | [`models.Categories`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/go/models/structures/categories.md) | Required | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    pagedCategories := models.PagedCategories{
        Categories:            models.Categories{
            Href:                  "https://api.spotify.com/v1/me/shows?offset=0&limit=20\n",
            Limit:                 20,
            Next:                  models.ToPointer("https://api.spotify.com/v1/me/shows?offset=1&limit=1"),
            Offset:                0,
            Previous:              models.ToPointer("https://api.spotify.com/v1/me/shows?offset=1&limit=1"),
            Total:                 4,
            Items:                 []models.CategoryObject{
                models.CategoryObject{
                    Href:                  "href0",
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
                },
            },
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        },
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



