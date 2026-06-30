# Cursor Paging Play History Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/net-standard-library/x-redirect/JTI0bSUyRkN1cnNvclBhZ2luZ1BsYXlIaXN0b3J5T2JqZWN0

*This model accepts additional fields of type object.*


# Class Name

`CursorPagingPlayHistoryObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Href` | `string` | Optional | A link to the Web API endpoint returning the full result of the request. |
| `Limit` | `int?` | Optional | The maximum number of items in the response (as set in the query or by default). |
| `Next` | `string` | Optional | URL to the next page of items. ( `null` if none) |
| `Cursors` | [`CursorObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/net-standard-library/models/structures/cursor-object.md) | Optional | The cursors used to find the next set of items. |
| `Total` | `int?` | Optional | The total number of items available to return. |
| `Items` | [`List<PlayHistoryObject>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/net-standard-library/models/structures/play-history-object.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models;
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Utilities;

CursorPagingPlayHistoryObject cursorPagingPlayHistoryObject = new CursorPagingPlayHistoryObject
{
    Href = "href2",
    Limit = 124,
    Next = "next8",
    Cursors = new CursorObject
    {
        After = "after8",
        Before = "before6",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    Total = 218,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



