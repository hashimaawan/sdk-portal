# Meta

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRk1ldGE

*This model accepts additional fields of type object.*


# Class Name

`Meta`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Pagination` | [`Pagination`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/pagination.md) | Required | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;

Meta meta = new Meta
{
    Pagination = new Pagination
    {
        LastPage = 4,
        NextPage = 4,
        Page = 3,
        PerPage = 25,
        PreviousPage = 2,
        TotalEntries = 100,
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



