# Placement Group Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlBsYWNlbWVudEdyb3VwUmVzcG9uc2U

*This model accepts additional fields of type object.*


# Class Name

`PlacementGroupResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `PlacementGroup` | [`PlacementGroup`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/placement-group.md) | Required | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;
using System.Collections.Generic;

PlacementGroupResponse placementGroupResponse = new PlacementGroupResponse
{
    PlacementGroup = new PlacementGroup
    {
        Created = "2016-01-30T23:55:00+00:00",
        Id = 42,
        Labels = new Dictionary<string, string>
        {
            ["key0"] = "labels4",
        },
        Name = "my-resource",
        Servers = new List<int>
        {
            42,
        },
        Type = "spread",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



