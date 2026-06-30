# Many Albums

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/net-standard-library/x-redirect/JTI0bSUyRk1hbnlBbGJ1bXM

*This model accepts additional fields of type object.*


# Class Name

`ManyAlbums`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Albums` | [`List<AlbumObject>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/net-standard-library/models/structures/album-object.md) | Required | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models;
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Utilities;
using System.Collections.Generic;

ManyAlbums manyAlbums = new ManyAlbums
{
    Albums = new List<AlbumObject>
    {
        new AlbumObject
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
            Tracks = new PagingSimplifiedTrackObject
            {
                Href = "https://api.spotify.com/v1/me/shows?offset=0&limit=20\n",
                Limit = 20,
                Next = "https://api.spotify.com/v1/me/shows?offset=1&limit=1",
                Offset = 0,
                Previous = "https://api.spotify.com/v1/me/shows?offset=1&limit=1",
                Total = 4,
                Items = new List<SimplifiedTrackObject>
                {
                    new SimplifiedTrackObject
                    {
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
                        AvailableMarkets = new List<string>
                        {
                            "available_markets2",
                        },
                        DiscNumber = 244,
                        DurationMs = 52,
                        MExplicit = false,
                        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                    },
                },
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            Copyrights = new List<CopyrightObject>
            {
                new CopyrightObject
                {
                    Text = "text2",
                    Type = "type2",
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
            },
            ExternalIds = new ExternalIdObject
            {
                Isrc = "isrc8",
                Ean = "ean8",
                Upc = "upc2",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            Genres = new List<string>
            {
                "Egg punk",
                "Noise rock",
            },
            Label = "label8",
            Popularity = 66,
            Restrictions = new AlbumRestrictionObject
            {
                Reason = Reason.Explicit,
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



