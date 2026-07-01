# Servers Actions Request Console Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMFJlcXVlc3QlMjUyMENvbnNvbGUlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type object.*


# Class Name

`ServersActionsRequestConsoleResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Action` | [`Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/action.md) | Required | - |
| `Password` | `string` | Required | VNC password to use for this connection (this password only works in combination with a wss_url with valid token) |
| `WssUrl` | `string` | Required | URL of websocket proxy to use; this includes a token which is valid for a limited time only |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;
using System.Collections.Generic;

ServersActionsRequestConsoleResponse serversActionsRequestConsoleResponse = new ServersActionsRequestConsoleResponse
{
    Action = new Action
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
    },
    Password = "9MQaTg2VAGI0FIpc10k3UpRXcHj2wQ6x",
    WssUrl = "wss://console.hetzner.cloud/?server_id=1&token=3db32d15-af2f-459c-8bf8-dee1fd05f49c",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



