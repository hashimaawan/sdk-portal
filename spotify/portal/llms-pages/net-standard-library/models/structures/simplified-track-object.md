# Simplified Track Object

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/net-standard-library/x-redirect/JTI0bSUyRlNpbXBsaWZpZWRUcmFja09iamVjdA

*This model accepts additional fields of type object.*


# Class Name

`SimplifiedTrackObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Artists` | [`List<SimplifiedArtistObject>`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/net-standard-library/models/structures/simplified-artist-object.md) | Optional | The artists who performed the track. Each artist object includes a link in `href` to more detailed information about the artist. |
| `AvailableMarkets` | `List<string>` | Optional | A list of the countries in which the track can be played, identified by their [ISO 3166-1 alpha-2](http://en.wikipedia.org/wiki/ISO_3166-1_alpha-2) code. |
| `DiscNumber` | `int?` | Optional | The disc number (usually `1` unless the album consists of more than one disc). |
| `DurationMs` | `int?` | Optional | The track length in milliseconds. |
| `Explicit` | `bool?` | Optional | Whether or not the track has explicit lyrics ( `true` = yes it does; `false` = no it does not OR unknown). |
| `ExternalUrls` | [`ExternalUrlObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/net-standard-library/models/structures/external-url-object.md) | Optional | External URLs for this track. |
| `Href` | `string` | Optional | A link to the Web API endpoint providing full details of the track. |
| `Id` | `string` | Optional | The [Spotify ID](/documentation/web-api/concepts/spotify-uris-ids) for the track. |
| `IsPlayable` | `bool?` | Optional | Part of the response when [Track Relinking](/documentation/web-api/concepts/track-relinking/) is applied. If `true`, the track is playable in the given market. Otherwise `false`. |
| `LinkedFrom` | [`LinkedTrackObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/net-standard-library/models/structures/linked-track-object.md) | Optional | Part of the response when [Track Relinking](/documentation/web-api/concepts/track-relinking/) is applied and is only part of the response if the track linking, in fact, exists. The requested track has been replaced with a different track. The track in the `linked_from` object contains information about the originally requested track. |
| `Restrictions` | [`TrackRestrictionObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/net-standard-library/models/structures/track-restriction-object.md) | Optional | Included in the response when a content restriction is applied. |
| `Name` | `string` | Optional | The name of the track. |
| `PreviewUrl` | `string` | Optional | A URL to a 30 second preview (MP3 format) of the track. |
| `TrackNumber` | `int?` | Optional | The number of the track. If an album has several discs, the track number is the number on the specified disc. |
| `Type` | `string` | Optional | The object type: "track". |
| `Uri` | `string` | Optional | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for the track. |
| `IsLocal` | `bool?` | Optional | Whether or not the track is from a local file. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models;
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Utilities;
using System.Collections.Generic;

SimplifiedTrackObject simplifiedTrackObject = new SimplifiedTrackObject
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
        "available_markets0",
        "available_markets1",
        "available_markets2",
    },
    DiscNumber = 180,
    DurationMs = 244,
    MExplicit = false,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



