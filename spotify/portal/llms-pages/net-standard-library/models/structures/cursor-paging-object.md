# Cursor Paging Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/net-standard-library/x-redirect/JTI0bSUyRkN1cnNvclBhZ2luZ09iamVjdA

*This model accepts additional fields of type object.*


# Class Name

`CursorPagingObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Href` | `string` | Optional | A link to the Web API endpoint returning the full result of the request. |
| `Limit` | `int?` | Optional | The maximum number of items in the response (as set in the query or by default). |
| `Next` | `string` | Optional | URL to the next page of items. ( `null` if none) |
| `Cursors` | [`CursorObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/net-standard-library/models/structures/cursor-object.md) | Optional | The cursors used to find the next set of items. |
| `Total` | `int?` | Optional | The total number of items available to return. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models;
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Utilities;

CursorPagingObject cursorPagingObject = new CursorPagingObject
{
    Href = "href8",
    Limit = 82,
    Next = "next6",
    Cursors = new CursorObject
    {
        After = "after8",
        Before = "before6",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    Total = 176,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



