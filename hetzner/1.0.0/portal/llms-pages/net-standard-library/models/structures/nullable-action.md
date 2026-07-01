# Nullable Action

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRk51bGxhYmxlQWN0aW9u

*This model accepts additional fields of type object.*


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
| `Status` | [`Status`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/enumerations/status.md) | Required | Status of the Action |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;
using System.Collections.Generic;

NullableAction nullableAction = new NullableAction
{
    Command = "start_server",
    Error = new Error
    {
        Code = "action_failed",
        Message = "Action failed",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
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
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    Started = "2016-01-30T23:55:00+00:00",
    Status = Status.Running,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



