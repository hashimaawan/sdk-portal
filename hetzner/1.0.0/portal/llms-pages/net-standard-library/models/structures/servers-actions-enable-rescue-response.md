# Servers Actions Enable Rescue Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMEVuYWJsZSUyNTIwUmVzY3VlJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type object.*


# Class Name

`ServersActionsEnableRescueResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Action` | [`Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/action.md) | Optional | - |
| `RootPassword` | `string` | Optional | Password that will be set for this Server once the Action succeeds |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;
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
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
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
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            new Resource
            {
                Id = 198,
                Type = "type0",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            new Resource
            {
                Id = 198,
                Type = "type0",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
        },
        Started = "started8",
        Status = Status.Running,
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    RootPassword = "zCWbFhnu950dUTko5f40",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



