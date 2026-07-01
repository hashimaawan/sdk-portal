# Create Placement Group Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkNyZWF0ZVBsYWNlbWVudEdyb3VwUmVzcG9uc2U


# Class Name

`CreatePlacementGroupResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Action` | [`NullableAction`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/nullable-action.md) | Optional | - |
| `PlacementGroup` | [`PlacementGroup`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/placement-group.md) | Required | - |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;
using System.Collections.Generic;

CreatePlacementGroupResponse createPlacementGroupResponse = new CreatePlacementGroupResponse
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
    },
    Action = new NullableAction
    {
        Command = "command6",
        Error = new Error
        {
            Code = "code2",
            Message = "message4",
        },
        Finished = "finished0",
        Id = 238,
        Progress = 143.26,
        Resources = new List<Resource>
        {
            new Resource
            {
                Id = 198,
                Type = "type0",
            },
            new Resource
            {
                Id = 198,
                Type = "type0",
            },
            new Resource
            {
                Id = 198,
                Type = "type0",
            },
        },
        Started = "started8",
        Status = StatusEnum.Running,
    },
};
```



