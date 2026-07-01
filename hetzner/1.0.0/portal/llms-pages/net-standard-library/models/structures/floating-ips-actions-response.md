# Floating Ips Actions Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkZsb2F0aW5nJTI1MjBJcHMlMjUyMEFjdGlvbnMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type object.*


# Class Name

`FloatingIpsActionsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Actions` | [`List<Action>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/action.md) | Required | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;
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
            Status = Status.Success,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



