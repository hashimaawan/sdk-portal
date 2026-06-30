# Album Object

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/go/x-redirect/JTI0bSUyRkFsYnVtT2JqZWN0

*This model accepts additional fields of type interface{}.*


# Class Name

`AlbumObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AlbumType` | [`models.AlbumType`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/go/models/enumerations/album-type.md) | Required | The type of the album. |
| `TotalTracks` | `int` | Required | The number of tracks in the album. |
| `AvailableMarkets` | `[]string` | Required | The markets in which the album is available: [ISO 3166-1 alpha-2 country codes](http://en.wikipedia.org/wiki/ISO_3166-1_alpha-2). _**NOTE**: an album is considered available in a market when at least 1 of its tracks is available in that market._ |
| `ExternalUrls` | [`models.ExternalUrlObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/go/models/structures/external-url-object.md) | Required | Known external URLs for this album. |
| `Href` | `string` | Required | A link to the Web API endpoint providing full details of the album. |
| `Id` | `string` | Required | The [Spotify ID](/documentation/web-api/concepts/spotify-uris-ids) for the album. |
| `Images` | [`[]models.ImageObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/go/models/structures/image-object.md) | Required | The cover art for the album in various sizes, widest first. |
| `Name` | `string` | Required | The name of the album. In case of an album takedown, the value may be an empty string. |
| `ReleaseDate` | `string` | Required | The date the album was first released. |
| `ReleaseDatePrecision` | [`models.ReleaseDatePrecision`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/go/models/enumerations/release-date-precision.md) | Required | The precision with which `release_date` value is known. |
| `Restrictions` | [`*models.AlbumRestrictionObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/go/models/structures/album-restriction-object.md) | Optional | Included in the response when a content restriction is applied. |
| `Type` | `string` | Required, Constant | The object type.<br><br>**Value**: `"album"` |
| `Uri` | `string` | Required | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for the album. |
| `Artists` | [`[]models.SimplifiedArtistObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/go/models/structures/simplified-artist-object.md) | Required | The artists of the album. Each artist object includes a link in `href` to more detailed information about the artist. |
| `Tracks` | [`models.PagingSimplifiedTrackObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/go/models/structures/paging-simplified-track-object.md) | Required | The tracks of the album. |
| `Copyrights` | [`[]models.CopyrightObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/go/models/structures/copyright-object.md) | Required | The copyright statements of the album. |
| `ExternalIds` | [`models.ExternalIdObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/go/models/structures/external-id-object.md) | Required | Known external IDs for the album. |
| `Genres` | `[]string` | Required | A list of the genres the album is associated with. If not yet classified, the array is empty. |
| `Label` | `string` | Required | The label associated with the album. |
| `Popularity` | `int` | Required | The popularity of the album. The value will be between 0 and 100, with 100 being the most popular. |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    albumObject := models.AlbumObject{
        AlbumType:             models.AlbumType_Compilation,
        TotalTracks:           9,
        AvailableMarkets:      []string{
            "CA",
            "BR",
            "IT",
        },
        ExternalUrls:          models.ExternalUrlObject{
            Spotify:               models.ToPointer("spotify6"),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        },
        Href:                  "href8",
        Id:                    "2up3OPMp9Tb4dAKM2erWXQ",
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
        Name:                  "name6",
        ReleaseDate:           "1981-12",
        ReleaseDatePrecision:  models.ReleaseDatePrecision_Year,
        Restrictions:          models.ToPointer(models.AlbumRestrictionObject{
            Reason:                models.ToPointer(models.Reason_Explicit),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        Type:                  "album",
        Uri:                   "spotify:album:2up3OPMp9Tb4dAKM2erWXQ",
        Artists:               []models.SimplifiedArtistObject{
            models.SimplifiedArtistObject{
                ExternalUrls:          models.ToPointer(models.ExternalUrlObject{
                    Spotify:               models.ToPointer("spotify6"),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                }),
                Href:                  models.ToPointer("href2"),
                Id:                    models.ToPointer("id0"),
                Name:                  models.ToPointer("name0"),
                Type:                  models.ToPointer(models.Type_Artist),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        Tracks:                models.PagingSimplifiedTrackObject{
            Href:                  "https://api.spotify.com/v1/me/shows?offset=0&limit=20\n",
            Limit:                 20,
            Next:                  models.ToPointer("https://api.spotify.com/v1/me/shows?offset=1&limit=1"),
            Offset:                0,
            Previous:              models.ToPointer("https://api.spotify.com/v1/me/shows?offset=1&limit=1"),
            Total:                 4,
            Items:                 []models.SimplifiedTrackObject{
                models.SimplifiedTrackObject{
                    Artists:               []models.SimplifiedArtistObject{
                        models.SimplifiedArtistObject{
                            ExternalUrls:          models.ToPointer(models.ExternalUrlObject{
                                Spotify:               models.ToPointer("spotify6"),
                                AdditionalProperties:  map[string]interface{}{
                                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                                },
                            }),
                            Href:                  models.ToPointer("href2"),
                            Id:                    models.ToPointer("id0"),
                            Name:                  models.ToPointer("name0"),
                            Type:                  models.ToPointer(models.Type_Artist),
                            AdditionalProperties:  map[string]interface{}{
                                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                            },
                        },
                    },
                    AvailableMarkets:      []string{
                        "available_markets2",
                    },
                    DiscNumber:            models.ToPointer(244),
                    DurationMs:            models.ToPointer(52),
                    Explicit:              models.ToPointer(false),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
            },
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
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
        ExternalIds:           models.ExternalIdObject{
            Isrc:                  models.ToPointer("isrc8"),
            Ean:                   models.ToPointer("ean8"),
            Upc:                   models.ToPointer("upc2"),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        },
        Genres:                []string{
            "Egg punk",
            "Noise rock",
        },
        Label:                 "label6",
        Popularity:            152,
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



