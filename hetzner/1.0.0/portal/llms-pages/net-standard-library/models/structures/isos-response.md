# Isos Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRklzb3MlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type object.*


# Class Name

`IsosResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Isos` | [`List<Iso>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/iso.md) | Required | - |
| `Meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/meta.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;
using System.Collections.Generic;

IsosResponse isosResponse = new IsosResponse
{
    Isos = new List<Iso>
    {
        new Iso
        {
            Deprecated = "2018-02-28T00:00:00+00:00",
            Description = "FreeBSD 11.0 x64",
            Id = 42,
            Name = "FreeBSD-11.0-RELEASE-amd64-dvd1",
            Type = Type26.Public,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    Meta = new Meta
    {
        Pagination = new Pagination
        {
            LastPage = 77.7,
            NextPage = 209.18,
            Page = 17.58,
            PerPage = 13.34,
            PreviousPage = 50.02,
            TotalEntries = 206.64,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



