# Audiobook Base

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/go/x-redirect/JTI0bSUyRkF1ZGlvYm9va0Jhc2U

*This model accepts additional fields of type interface{}.*


# Class Name

`AudiobookBase`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Authors` | [`[]models.AuthorObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/go/models/structures/author-object.md) | Required | The author(s) for the audiobook. |
| `AvailableMarkets` | `[]string` | Required | A list of the countries in which the audiobook can be played, identified by their [ISO 3166-1 alpha-2](http://en.wikipedia.org/wiki/ISO_3166-1_alpha-2) code. |
| `Copyrights` | [`[]models.CopyrightObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/go/models/structures/copyright-object.md) | Required | The copyright statements of the audiobook. |
| `Description` | `string` | Required | A description of the audiobook. HTML tags are stripped away from this field, use `html_description` field in case HTML tags are needed. |
| `HtmlDescription` | `string` | Required | A description of the audiobook. This field may contain HTML tags. |
| `Edition` | `*string` | Optional | The edition of the audiobook. |
| `Explicit` | `bool` | Required | Whether or not the audiobook has explicit content (true = yes it does; false = no it does not OR unknown). |
| `ExternalUrls` | [`models.ExternalUrlObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/go/models/structures/external-url-object.md) | Required | External URLs for this audiobook. |
| `Href` | `string` | Required | A link to the Web API endpoint providing full details of the audiobook. |
| `Id` | `string` | Required | The [Spotify ID](/documentation/web-api/concepts/spotify-uris-ids) for the audiobook. |
| `Images` | [`[]models.ImageObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/go/models/structures/image-object.md) | Required | The cover art for the audiobook in various sizes, widest first. |
| `Languages` | `[]string` | Required | A list of the languages used in the audiobook, identified by their [ISO 639](https://en.wikipedia.org/wiki/ISO_639) code. |
| `MediaType` | `string` | Required | The media type of the audiobook. |
| `Name` | `string` | Required | The name of the audiobook. |
| `Narrators` | [`[]models.NarratorObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/go/models/structures/narrator-object.md) | Required | The narrator(s) for the audiobook. |
| `Publisher` | `string` | Required | The publisher of the audiobook. |
| `Type` | `string` | Required, Constant | The object type.<br><br>**Value**: `"audiobook"` |
| `Uri` | `string` | Required | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for the audiobook. |
| `TotalChapters` | `int` | Required | The number of chapters in this audiobook. |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    audiobookBase := models.AudiobookBase{
        Authors:               []models.AuthorObject{
            models.AuthorObject{
                Name:                  models.ToPointer("name0"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        AvailableMarkets:      []string{
            "available_markets4",
            "available_markets5",
            "available_markets6",
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
        Description:           "description0",
        HtmlDescription:       "html_description0",
        Edition:               models.ToPointer("Unabridged"),
        Explicit:              false,
        ExternalUrls:          models.ExternalUrlObject{
            Spotify:               models.ToPointer("spotify6"),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        },
        Href:                  "href2",
        Id:                    "id0",
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
        Languages:             []string{
            "languages7",
            "languages8",
            "languages9",
        },
        MediaType:             "media_type2",
        Name:                  "name0",
        Narrators:             []models.NarratorObject{
            models.NarratorObject{
                Name:                  models.ToPointer("name0"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        Publisher:             "publisher2",
        Type:                  "audiobook",
        Uri:                   "uri4",
        TotalChapters:         120,
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



