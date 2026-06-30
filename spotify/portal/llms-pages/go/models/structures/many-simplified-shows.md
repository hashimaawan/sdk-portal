# Many Simplified Shows

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/go/x-redirect/JTI0bSUyRk1hbnlTaW1wbGlmaWVkU2hvd3M

*This model accepts additional fields of type interface{}.*


# Class Name

`ManySimplifiedShows`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Shows` | [`[]models.ShowBase`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/go/models/structures/show-base.md) | Required | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    manySimplifiedShows := models.ManySimplifiedShows{
        Shows:                 []models.ShowBase{
            models.ShowBase{
                AvailableMarkets:      []string{
                    "available_markets2",
                },
                Copyrights:            []models.CopyrightObject{
                    models.CopyrightObject{
                        Text:                  models.ToPointer("text2"),
                        Type:                  models.ToPointer("type2"),
                        AdditionalProperties:  map[string]interface{}{
                            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                        },
                    },
                },
                Description:           "description8",
                HtmlDescription:       "html_description2",
                Explicit:              false,
                ExternalUrls:          models.ExternalUrlObject{
                    Spotify:               models.ToPointer("spotify6"),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
                Href:                  "href0",
                Id:                    "id8",
                Images:                []models.ImageObject{
                    models.ImageObject{
                        Url:                   "https://i.scdn.co/image/ab67616d00001e02ff9ca10b55ce82ae553c8228\n",
                        Height:                models.ToPointer(300),
                        Width:                 models.ToPointer(300),
                        AdditionalProperties:  map[string]interface{}{
                            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                        },
                    },
                },
                IsExternallyHosted:    false,
                Languages:             []string{
                    "languages5",
                },
                MediaType:             "media_type4",
                Name:                  "name8",
                Publisher:             "publisher4",
                Type:                  "show",
                Uri:                   "uri2",
                TotalEpisodes:         196,
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



