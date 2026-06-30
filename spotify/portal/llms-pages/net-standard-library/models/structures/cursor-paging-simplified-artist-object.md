# Cursor Paging Simplified Artist Object

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/net-standard-library/x-redirect/JTI0bSUyRkN1cnNvclBhZ2luZ1NpbXBsaWZpZWRBcnRpc3RPYmplY3Q

*This model accepts additional fields of type object.*


# Class Name

`CursorPagingSimplifiedArtistObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Href` | `string` | Optional | A link to the Web API endpoint returning the full result of the request. |
| `Limit` | `int?` | Optional | The maximum number of items in the response (as set in the query or by default). |
| `Next` | `string` | Optional | URL to the next page of items. ( `null` if none) |
| `Cursors` | [`CursorObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/net-standard-library/models/structures/cursor-object.md) | Optional | The cursors used to find the next set of items. |
| `Total` | `int?` | Optional | The total number of items available to return. |
| `Items` | [`List<ArtistObject>`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/net-standard-library/models/structures/artist-object.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models;
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Utilities;

CursorPagingSimplifiedArtistObject cursorPagingSimplifiedArtistObject = new CursorPagingSimplifiedArtistObject
{
    Href = "href2",
    Limit = 24,
    Next = "next2",
    Cursors = new CursorObject
    {
        After = "after8",
        Before = "before6",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    Total = 118,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



