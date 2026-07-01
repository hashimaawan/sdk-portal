# Nullable Action

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRk51bGxhYmxlQWN0aW9u


# Class Name

`NullableAction`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Command` | `string` | Required | Command executed in the Action |
| `Error` | [`Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/error.md) | Required | Error message for the Action if error occurred, otherwise null |
| `Finished` | `string` | Required | Point in time when the Action was finished (in ISO-8601 format). Only set if the Action is finished otherwise null. |
| `Id` | `int` | Required | ID of the Resource |
| `Progress` | `double` | Required | Progress of Action in percent |
| `Resources` | [`List<Resource>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/resource.md) | Required | Resources the Action relates to |
| `Started` | `string` | Required | Point in time when the Action was started (in ISO-8601 format) |
| `Status` | [`StatusEnum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/enumerations/status.md) | Required | Status of the Action |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;
using System.Collections.Generic;

NullableAction nullableAction = new NullableAction
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
    Status = StatusEnum.Running,
};
```



