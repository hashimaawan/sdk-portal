# Servers Actions Request Console Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMFJlcXVlc3QlMjUyMENvbnNvbGUlMjUyMFJlc3BvbnNl


# Class Name

`ServersActionsRequestConsoleResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Action` | [`Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/action.md) | Required | - |
| `Password` | `string` | Required | VNC password to use for this connection (this password only works in combination with a wss_url with valid token) |
| `WssUrl` | `string` | Required | URL of websocket proxy to use; this includes a token which is valid for a limited time only |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;
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
    },
    Password = "9MQaTg2VAGI0FIpc10k3UpRXcHj2wQ6x",
    WssUrl = "wss://console.hetzner.cloud/?server_id=1&token=3db32d15-af2f-459c-8bf8-dee1fd05f49c",
};
```



