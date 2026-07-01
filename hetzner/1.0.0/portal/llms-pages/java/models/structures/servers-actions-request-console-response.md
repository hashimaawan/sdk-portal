# Servers Actions Request Console Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMFJlcXVlc3QlMjUyMENvbnNvbGUlMjUyMFJlc3BvbnNl


# Class Name

`ServersActionsRequestConsoleResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Action` | [`Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/action.md) | Required | - | Action getAction() | setAction(Action action) |
| `Password` | `String` | Required | VNC password to use for this connection (this password only works in combination with a wss_url with valid token) | String getPassword() | setPassword(String password) |
| `WssUrl` | `String` | Required | URL of websocket proxy to use; this includes a token which is valid for a limited time only | String getWssUrl() | setWssUrl(String wssUrl) |


# Example

```java
import cloud.hetzner.api.models.Action;
import cloud.hetzner.api.models.Error;
import cloud.hetzner.api.models.Resource;
import cloud.hetzner.api.models.ServersActionsRequestConsoleResponse;
import cloud.hetzner.api.models.StatusEnum;
import java.util.Arrays;

ServersActionsRequestConsoleResponse serversActionsRequestConsoleResponse = new ServersActionsRequestConsoleResponse.Builder(
    new Action.Builder(
        "start_server",
        new Error.Builder(
            "action_failed",
            "Action failed"
        )
        .build(),
        "2016-01-30T23:55:00+00:00",
        42,
        100D,
        Arrays.asList(
            new Resource.Builder(
                42,
                "server"
            )
            .build()
        ),
        "2016-01-30T23:55:00+00:00",
        StatusEnum.RUNNING
    )
    .build(),
    "9MQaTg2VAGI0FIpc10k3UpRXcHj2wQ6x",
    "wss://console.hetzner.cloud/?server_id=1&token=3db32d15-af2f-459c-8bf8-dee1fd05f49c"
)
.build();
```



