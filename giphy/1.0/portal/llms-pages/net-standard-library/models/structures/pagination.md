# Pagination

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlBhZ2luYXRpb24

The Pagination Object contains information relating to the number of total results available as well as the number of results fetched and their relative positions.

*This model accepts additional fields of type object.*


# Class Name

`Pagination`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Count` | `int?` | Optional | Total number of items returned. |
| `Offset` | `int?` | Optional | Position in pagination. |
| `TotalCount` | `int?` | Optional | Total number of items available. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using GiphyApi.Standard.Models;
using GiphyApi.Standard.Utilities;

Pagination pagination = new Pagination
{
    Count = 25,
    Offset = 75,
    TotalCount = 250,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



