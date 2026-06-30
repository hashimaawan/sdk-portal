# Search Items

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/go/x-redirect/JTI0bSUyRlNlYXJjaEl0ZW1z

*This model accepts additional fields of type interface{}.*


# Class Name

`SearchItems`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Tracks` | [`*models.PagingTrackObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/go/models/structures/paging-track-object.md) | Optional | - |
| `Artists` | [`*models.PagingArtistObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/go/models/structures/paging-artist-object.md) | Optional | - |
| `Albums` | [`*models.PagingSimplifiedAlbumObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/go/models/structures/paging-simplified-album-object.md) | Optional | - |
| `Playlists` | [`*models.PagingPlaylistObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/go/models/structures/paging-playlist-object.md) | Optional | - |
| `Shows` | [`*models.PagingSimplifiedShowObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/go/models/structures/paging-simplified-show-object.md) | Optional | - |
| `Episodes` | [`*models.PagingSimplifiedEpisodeObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/go/models/structures/paging-simplified-episode-object.md) | Optional | - |
| `Audiobooks` | [`*models.PagingSimplifiedAudiobookObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/go/models/structures/paging-simplified-audiobook-object.md) | Optional | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    searchItems := models.SearchItems{
        Tracks:                models.ToPointer(models.PagingTrackObject{
            Href:                  "href6",
            Limit:                 142,
            Next:                  models.ToPointer("next8"),
            Offset:                238,
            Previous:              models.ToPointer("previous2"),
            Total:                 236,
            Items:                 []models.TrackObject{
                models.TrackObject{
                    Album:                 models.ToPointer(models.SimplifiedAlbumObject{
                        AlbumType:             models.AlbumType_Single,
                        TotalTracks:           170,
                        AvailableMarkets:      []string{
                            "available_markets2",
                            "available_markets3",
                        },
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
                                Url:                   "url6",
                                Height:                models.ToPointer(182),
                                Width:                 models.ToPointer(222),
                                AdditionalProperties:  map[string]interface{}{
                                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                                },
                            },
                        },
                        Name:                  "name8",
                        ReleaseDate:           "release_date6",
                        ReleaseDatePrecision:  models.ReleaseDatePrecision_Day,
                        Restrictions:          models.ToPointer(models.AlbumRestrictionObject{
                            Reason:                models.ToPointer(models.Reason_Explicit),
                            AdditionalProperties:  map[string]interface{}{
                                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                            },
                        }),
                        Type:                  "type2",
                        Uri:                   "uri2",
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
                        AdditionalProperties:  map[string]interface{}{
                            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                        },
                    }),
                    Artists:               []models.ArtistObject{
                        models.ArtistObject{
                            ExternalUrls:          models.ToPointer(models.ExternalUrlObject{
                                Spotify:               models.ToPointer("spotify6"),
                                AdditionalProperties:  map[string]interface{}{
                                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                                },
                            }),
                            Followers:             models.ToPointer(models.FollowersObject{
                                Href:                  models.NewOptional(models.ToPointer("href0")),
                                Total:                 models.ToPointer(82),
                                AdditionalProperties:  map[string]interface{}{
                                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                                },
                            }),
                            Genres:                []string{
                                "genres7",
                                "genres8",
                            },
                            Href:                  models.ToPointer("href2"),
                            Id:                    models.ToPointer("id0"),
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
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
            },
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        Artists:               models.ToPointer(models.PagingArtistObject{
            Href:                  "href2",
            Limit:                 214,
            Next:                  models.ToPointer("next2"),
            Offset:                54,
            Previous:              models.ToPointer("previous8"),
            Total:                 52,
            Items:                 []models.ArtistObject{
                models.ArtistObject{
                    ExternalUrls:          models.ToPointer(models.ExternalUrlObject{
                        Spotify:               models.ToPointer("spotify6"),
                        AdditionalProperties:  map[string]interface{}{
                            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                        },
                    }),
                    Followers:             models.ToPointer(models.FollowersObject{
                        Href:                  models.NewOptional(models.ToPointer("href0")),
                        Total:                 models.ToPointer(82),
                        AdditionalProperties:  map[string]interface{}{
                            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                        },
                    }),
                    Genres:                []string{
                        "genres5",
                        "genres6",
                    },
                    Href:                  models.ToPointer("href0"),
                    Id:                    models.ToPointer("id8"),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
                models.ArtistObject{
                    ExternalUrls:          models.ToPointer(models.ExternalUrlObject{
                        Spotify:               models.ToPointer("spotify6"),
                        AdditionalProperties:  map[string]interface{}{
                            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                        },
                    }),
                    Followers:             models.ToPointer(models.FollowersObject{
                        Href:                  models.NewOptional(models.ToPointer("href0")),
                        Total:                 models.ToPointer(82),
                        AdditionalProperties:  map[string]interface{}{
                            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                        },
                    }),
                    Genres:                []string{
                        "genres5",
                        "genres6",
                    },
                    Href:                  models.ToPointer("href0"),
                    Id:                    models.ToPointer("id8"),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
                models.ArtistObject{
                    ExternalUrls:          models.ToPointer(models.ExternalUrlObject{
                        Spotify:               models.ToPointer("spotify6"),
                        AdditionalProperties:  map[string]interface{}{
                            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                        },
                    }),
                    Followers:             models.ToPointer(models.FollowersObject{
                        Href:                  models.NewOptional(models.ToPointer("href0")),
                        Total:                 models.ToPointer(82),
                        AdditionalProperties:  map[string]interface{}{
                            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                        },
                    }),
                    Genres:                []string{
                        "genres5",
                        "genres6",
                    },
                    Href:                  models.ToPointer("href0"),
                    Id:                    models.ToPointer("id8"),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
            },
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        Albums:                models.ToPointer(models.PagingSimplifiedAlbumObject{
            Href:                  "href0",
            Limit:                 0,
            Next:                  models.ToPointer("next4"),
            Offset:                96,
            Previous:              models.ToPointer("previous6"),
            Total:                 94,
            Items:                 []models.SimplifiedAlbumObject{
                models.SimplifiedAlbumObject{
                    AlbumType:             models.AlbumType_Album,
                    TotalTracks:           196,
                    AvailableMarkets:      []string{
                        "available_markets2",
                    },
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
                            Url:                   "url6",
                            Height:                models.ToPointer(182),
                            Width:                 models.ToPointer(222),
                            AdditionalProperties:  map[string]interface{}{
                                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                            },
                        },
                        models.ImageObject{
                            Url:                   "url6",
                            Height:                models.ToPointer(182),
                            Width:                 models.ToPointer(222),
                            AdditionalProperties:  map[string]interface{}{
                                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                            },
                        },
                    },
                    Name:                  "name8",
                    ReleaseDate:           "release_date6",
                    ReleaseDatePrecision:  models.ReleaseDatePrecision_Month,
                    Restrictions:          models.ToPointer(models.AlbumRestrictionObject{
                        Reason:                models.ToPointer(models.Reason_Explicit),
                        AdditionalProperties:  map[string]interface{}{
                            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                        },
                    }),
                    Type:                  "type2",
                    Uri:                   "uri2",
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
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
            },
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        Playlists:             models.ToPointer(models.PagingPlaylistObject{
            Href:                  "href2",
            Limit:                 68,
            Next:                  models.ToPointer("next2"),
            Offset:                164,
            Previous:              models.ToPointer("previous8"),
            Total:                 162,
            Items:                 []models.SimplifiedPlaylistObject{
                models.SimplifiedPlaylistObject{
                    Collaborative:         models.ToPointer(false),
                    Description:           models.ToPointer("description2"),
                    ExternalUrls:          models.ToPointer(models.ExternalUrlObject{
                        Spotify:               models.ToPointer("spotify6"),
                        AdditionalProperties:  map[string]interface{}{
                            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                        },
                    }),
                    Href:                  models.ToPointer("href0"),
                    Id:                    models.ToPointer("id8"),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
                models.SimplifiedPlaylistObject{
                    Collaborative:         models.ToPointer(false),
                    Description:           models.ToPointer("description2"),
                    ExternalUrls:          models.ToPointer(models.ExternalUrlObject{
                        Spotify:               models.ToPointer("spotify6"),
                        AdditionalProperties:  map[string]interface{}{
                            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                        },
                    }),
                    Href:                  models.ToPointer("href0"),
                    Id:                    models.ToPointer("id8"),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
                models.SimplifiedPlaylistObject{
                    Collaborative:         models.ToPointer(false),
                    Description:           models.ToPointer("description2"),
                    ExternalUrls:          models.ToPointer(models.ExternalUrlObject{
                        Spotify:               models.ToPointer("spotify6"),
                        AdditionalProperties:  map[string]interface{}{
                            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                        },
                    }),
                    Href:                  models.ToPointer("href0"),
                    Id:                    models.ToPointer("id8"),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
            },
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        Shows:                 models.ToPointer(models.PagingSimplifiedShowObject{
            Href:                  "href0",
            Limit:                 248,
            Next:                  models.ToPointer("next6"),
            Offset:                88,
            Previous:              models.ToPointer("previous6"),
            Total:                 86,
            Items:                 []models.ShowBase{
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
                            Url:                   "url6",
                            Height:                models.ToPointer(182),
                            Width:                 models.ToPointer(222),
                            AdditionalProperties:  map[string]interface{}{
                                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                            },
                        },
                        models.ImageObject{
                            Url:                   "url6",
                            Height:                models.ToPointer(182),
                            Width:                 models.ToPointer(222),
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
                    Type:                  "type2",
                    Uri:                   "uri2",
                    TotalEpisodes:         166,
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
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
                            Url:                   "url6",
                            Height:                models.ToPointer(182),
                            Width:                 models.ToPointer(222),
                            AdditionalProperties:  map[string]interface{}{
                                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                            },
                        },
                        models.ImageObject{
                            Url:                   "url6",
                            Height:                models.ToPointer(182),
                            Width:                 models.ToPointer(222),
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
                    Type:                  "type2",
                    Uri:                   "uri2",
                    TotalEpisodes:         166,
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
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
                            Url:                   "url6",
                            Height:                models.ToPointer(182),
                            Width:                 models.ToPointer(222),
                            AdditionalProperties:  map[string]interface{}{
                                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                            },
                        },
                        models.ImageObject{
                            Url:                   "url6",
                            Height:                models.ToPointer(182),
                            Width:                 models.ToPointer(222),
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
                    Type:                  "type2",
                    Uri:                   "uri2",
                    TotalEpisodes:         166,
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
            },
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



