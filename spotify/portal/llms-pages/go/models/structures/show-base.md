# Show Base

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/go/x-redirect/JTI0bSUyRlNob3dCYXNl

*This model accepts additional fields of type interface{}.*


# Class Name

`ShowBase`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AvailableMarkets` | `[]string` | Required | A list of the countries in which the show can be played, identified by their [ISO 3166-1 alpha-2](http://en.wikipedia.org/wiki/ISO_3166-1_alpha-2) code. |
| `Copyrights` | [`[]models.CopyrightObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/go/models/structures/copyright-object.md) | Required | The copyright statements of the show. |
| `Description` | `string` | Required | A description of the show. HTML tags are stripped away from this field, use `html_description` field in case HTML tags are needed. |
| `HtmlDescription` | `string` | Required | A description of the show. This field may contain HTML tags. |
| `Explicit` | `bool` | Required | Whether or not the show has explicit content (true = yes it does; false = no it does not OR unknown). |
| `ExternalUrls` | [`models.ExternalUrlObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/go/models/structures/external-url-object.md) | Required | External URLs for this show. |
| `Href` | `string` | Required | A link to the Web API endpoint providing full details of the show. |
| `Id` | `string` | Required | The [Spotify ID](/documentation/web-api/concepts/spotify-uris-ids) for the show. |
| `Images` | [`[]models.ImageObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/go/models/structures/image-object.md) | Required | The cover art for the show in various sizes, widest first. |
| `IsExternallyHosted` | `bool` | Required | True if all of the shows episodes are hosted outside of Spotify's CDN. This field might be `null` in some cases. |
| `Languages` | `[]string` | Required | A list of the languages used in the show, identified by their [ISO 639](https://en.wikipedia.org/wiki/ISO_639) code. |
| `MediaType` | `string` | Required | The media type of the show. |
| `Name` | `string` | Required | The name of the episode. |
| `Publisher` | `string` | Required | The publisher of the show. |
| `Type` | `string` | Required, Constant | The object type.<br><br>**Value**: `"show"` |
| `Uri` | `string` | Required | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for the show. |
| `TotalEpisodes` | `int` | Required | The total number of episodes in the show. |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    showBase := models.ShowBase{
        AvailableMarkets:      []string{
            "available_markets2",
            "available_markets3",
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
        Description:           "description2",
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
            "languages3",
            "languages4",
            "languages5",
        },
        MediaType:             "media_type4",
        Name:                  "name8",
        Publisher:             "publisher4",
        Type:                  "show",
        Uri:                   "uri2",
        TotalEpisodes:         144,
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



