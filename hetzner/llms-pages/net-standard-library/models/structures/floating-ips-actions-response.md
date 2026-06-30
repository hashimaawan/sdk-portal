# Floating Ips Actions Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0bSUyRkZsb2F0aW5nJTI1MjBJcHMlMjUyMEFjdGlvbnMlMjUyMFJlc3BvbnNl


# Class Name

`FloatingIpsActionsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Actions` | [`List<Action>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/action.md) | Required | - |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;
using System.Collections.Generic;

FloatingIpsActionsResponse floatingIpsActionsResponse = new FloatingIpsActionsResponse
{
    Actions = new List<Action>
    {
        new Action
        {
            Command = "start_server",
            Error = new Error
            {
                Code = "action_failed",
                Message = "Action failed",
            },
            Finished = "2016-01-30T23:55:00+00:00",
            Id = 42,
            Progress = 100,
            Resources = new List<Resource>
            {
                new Resource
                {
                    Id = 42,
                    Type = "server",
                },
            },
            Started = "2016-01-30T23:55:00+00:00",
            Status = StatusEnum.Success,
        },
    },
};
```



