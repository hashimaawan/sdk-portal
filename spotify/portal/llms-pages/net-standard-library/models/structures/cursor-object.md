# Cursor Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/net-standard-library/x-redirect/JTI0bSUyRkN1cnNvck9iamVjdA

*This model accepts additional fields of type object.*


# Class Name

`CursorObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `After` | `string` | Optional | The cursor to use as key to find the next page of items. |
| `Before` | `string` | Optional | The cursor to use as key to find the previous page of items. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models;
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Utilities;

CursorObject cursorObject = new CursorObject
{
    After = "after0",
    Before = "before8",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



