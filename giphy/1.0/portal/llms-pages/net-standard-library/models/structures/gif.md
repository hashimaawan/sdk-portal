# Gif

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkdpZg

*This model accepts additional fields of type object.*


# Class Name

`Gif`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `BitlyUrl` | `string` | Optional | The unique bit.ly URL for this GIF |
| `ContentUrl` | `string` | Optional | Currently unused |
| `CreateDatetime` | `DateTime?` | Optional | The date this GIF was added to the GIPHY database. |
| `EmbdedUrl` | `string` | Optional | A URL used for embedding this GIF |
| `FeaturedTags` | `List<string>` | Optional | An array of featured tags for this GIF (Note: Not available when using the Public Beta Key) |
| `Id` | `string` | Optional | This GIF's unique ID |
| `Images` | [`Images`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/net-standard-library/models/structures/images.md) | Optional | An object containing data for various available formats and sizes of this GIF. |
| `ImportDatetime` | `DateTime?` | Optional | The creation or upload date from this GIF's source. |
| `Rating` | `string` | Optional | The MPAA-style rating for this content. Examples include Y, G, PG, PG-13 and R |
| `Slug` | `string` | Optional | The unique slug used in this GIF's URL |
| `Source` | `string` | Optional | The page on which this GIF was found |
| `SourcePostUrl` | `string` | Optional | The URL of the webpage on which this GIF was found. |
| `SourceTld` | `string` | Optional | The top level domain of the source URL. |
| `Tags` | `List<string>` | Optional | An array of tags for this GIF (Note: Not available when using the Public Beta Key) |
| `TrendingDatetime` | `DateTime?` | Optional | The date on which this gif was marked trending, if applicable. |
| `Type` | [`Type?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/net-standard-library/models/enumerations/type.md) | Optional | Type of the gif. By default, this is almost always gif<br><br>**Default**: `Type.gif` |
| `UpdateDatetime` | `DateTime?` | Optional | The date on which this GIF was last updated. |
| `Url` | `string` | Optional | The unique URL for this GIF |
| `User` | [`User`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/net-standard-library/models/structures/user.md) | Optional | The User Object contains information about the user associated with a GIF and URLs to assets such as that user's avatar image, profile, and more. |
| `Username` | `string` | Optional | The username this GIF is attached to, if applicable |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using GiphyApi.Standard.Models;
using GiphyApi.Standard.Utilities;
using System.Collections.Generic;
using System.Globalization;

Gif gif = new Gif
{
    BitlyUrl = "http://gph.is/1gsWDcL",
    ContentUrl = "content_url4",
    CreateDatetime = DateTime.ParseExact("2013-08-01 12:41:48", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    EmbdedUrl = "http://giphy.com/embed/YsTs5ltWtEhnq",
    FeaturedTags = new List<string>
    {
        "featured_tags0",
    },
    Id = "YsTs5ltWtEhnq",
    ImportDatetime = DateTime.ParseExact("2013-08-01 12:41:48", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    Rating = "g",
    Slug = "confused-flying-YsTs5ltWtEhnq",
    Source = "http://www.reddit.com/r/reactiongifs/comments/1xpyaa/superman_goes_to_hollywood/",
    SourcePostUrl = "http://cheezburger.com/5282328320",
    SourceTld = "cheezburger.com",
    TrendingDatetime = DateTime.ParseExact("2013-08-01 12:41:48", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    Type = GiphyApi.Standard.Models.Type.Gif,
    UpdateDatetime = DateTime.ParseExact("2013-08-01 12:41:48", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    Url = "http://giphy.com/gifs/confused-flying-YsTs5ltWtEhnq",
    Username = "JoeCool4000",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



