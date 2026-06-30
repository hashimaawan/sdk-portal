# Placement Groups Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0bSUyRlBsYWNlbWVudEdyb3Vwc1Jlc3BvbnNl


# Class Name

`PlacementGroupsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/meta.md) | Optional | - |
| `PlacementGroups` | [`List<PlacementGroup>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/placement-group.md) | Required | - |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;
using System.Collections.Generic;

PlacementGroupsResponse placementGroupsResponse = new PlacementGroupsResponse
{
    PlacementGroups = new List<PlacementGroup>
    {
        new PlacementGroup
        {
            Created = "2016-01-30T23:55:00+00:00",
            Id = 42,
            Labels = new Dictionary<string, string>
            {
                ["key0"] = "labels0",
                ["key1"] = "labels1",
            },
            Name = "my-resource",
            Servers = new List<int>
            {
                42,
            },
            Type = "spread",
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
        },
    },
};
```



