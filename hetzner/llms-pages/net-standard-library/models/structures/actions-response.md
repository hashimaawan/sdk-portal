# Actions Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0bSUyRkFjdGlvbnNSZXNwb25zZQ


# Class Name

`ActionsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Actions` | [`List<Action>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/action.md) | Required | - |
| `Meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/meta.md) | Optional | - |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;
using System.Collections.Generic;

ActionsResponse actionsResponse = new ActionsResponse
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



