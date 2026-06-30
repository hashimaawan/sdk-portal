# Paged Albums

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/net-standard-library/x-redirect/JTI0bSUyRlBhZ2VkQWxidW1z

*This model accepts additional fields of type object.*


# Class Name

`PagedAlbums`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Albums` | [`PagingSimplifiedAlbumObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/net-standard-library/models/structures/paging-simplified-album-object.md) | Required | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models;
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Utilities;
using System.Collections.Generic;

PagedAlbums pagedAlbums = new PagedAlbums
{
    Albums = new PagingSimplifiedAlbumObject
    {
        Href = "https://api.spotify.com/v1/me/shows?offset=0&limit=20\n",
        Limit = 20,
        Next = "https://api.spotify.com/v1/me/shows?offset=1&limit=1",
        Offset = 0,
        Previous = "https://api.spotify.com/v1/me/shows?offset=1&limit=1",
        Total = 4,
        Items = new List<SimplifiedAlbumObject>
        {
            new SimplifiedAlbumObject
            {
                AlbumType = AlbumType.Compilation,
                TotalTracks = 9,
                AvailableMarkets = new List<string>
                {
                    "CA",
                    "BR",
                    "IT",
                },
                ExternalUrls = new ExternalUrlObject
                {
                    Spotify = "spotify6",
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
                Href = "href0",
                Id = "2up3OPMp9Tb4dAKM2erWXQ",
                Images = new List<ImageObject>
                {
                    new ImageObject
                    {
                        Url = "https://i.scdn.co/image/ab67616d00001e02ff9ca10b55ce82ae553c8228\n",
                        Height = 300,
                        Width = 300,
                        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                    },
                },
                Name = "name8",
                ReleaseDate = "1981-12",
                ReleaseDatePrecision = ReleaseDatePrecision.Year,
                Type = "album",
                Uri = "spotify:album:2up3OPMp9Tb4dAKM2erWXQ",
                Artists = new List<SimplifiedArtistObject>
                {
                    new SimplifiedArtistObject
                    {
                        ExternalUrls = new ExternalUrlObject
                        {
                            Spotify = "spotify6",
                            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                        },
                        Href = "href2",
                        Id = "id0",
                        Name = "name0",
                        Type = SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models.Type.Artist,
                        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                    },
                },
                Restrictions = new AlbumRestrictionObject
                {
                    Reason = Reason.Explicit,
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
        },
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



