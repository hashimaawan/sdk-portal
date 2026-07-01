# Servers Actions Request Console Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMFJlcXVlc3QlMjUyMENvbnNvbGUlMjUyMFJlc3BvbnNl


# Class Name

`ServersActionsRequestConsoleResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Action` | [`models.Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/action.md) | Required | - |
| `Password` | `string` | Required | VNC password to use for this connection (this password only works in combination with a wss_url with valid token) |
| `WssUrl` | `string` | Required | URL of websocket proxy to use; this includes a token which is valid for a limited time only |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    serversActionsRequestConsoleResponse := models.ServersActionsRequestConsoleResponse{
        Action:               models.Action{
            Command:              "start_server",
            Error:                models.ToPointer(models.Error{
                Code:                 "action_failed",
                Message:              "Action failed",
            }),
            Finished:             models.ToPointer("2016-01-30T23:55:00+00:00"),
            Id:                   42,
            Progress:             float64(100),
            Resources:            []models.Resource{
                models.Resource{
                    Id:                   42,
                    Type:                 "server",
                },
            },
            Started:              "2016-01-30T23:55:00+00:00",
            Status:               models.StatusEnum_RUNNING,
        },
        Password:             "9MQaTg2VAGI0FIpc10k3UpRXcHj2wQ6x",
        WssUrl:               "wss://console.hetzner.cloud/?server_id=1&token=3db32d15-af2f-459c-8bf8-dee1fd05f49c",
    }

}
```



