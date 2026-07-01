# Servers Actions Enable Rescue Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMEVuYWJsZSUyNTIwUmVzY3VlJTI1MjBSZXNwb25zZQ


# Class Name

`ServersActionsEnableRescueResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Action` | [`Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/action.md) | Optional | - |
| `RootPassword` | `string` | Optional | Password that will be set for this Server once the Action succeeds |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;
using System.Collections.Generic;

ServersActionsEnableRescueResponse serversActionsEnableRescueResponse = new ServersActionsEnableRescueResponse
{
    Action = new Action
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
    RootPassword = "zCWbFhnu950dUTko5f40",
};
```



