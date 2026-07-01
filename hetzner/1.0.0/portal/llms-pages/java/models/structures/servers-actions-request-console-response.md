# Servers Actions Request Console Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMFJlcXVlc3QlMjUyMENvbnNvbGUlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type Object.*


# Class Name

`ServersActionsRequestConsoleResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Action` | [`Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/action.md) | Required | - | Action getAction() | setAction(Action action) |
| `Password` | `String` | Required | VNC password to use for this connection (this password only works in combination with a wss_url with valid token) | String getPassword() | setPassword(String password) |
| `WssUrl` | `String` | Required | URL of websocket proxy to use; this includes a token which is valid for a limited time only | String getWssUrl() | setWssUrl(String wssUrl) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.Action;
import cloud.hetzner.api.models.Error;
import cloud.hetzner.api.models.Resource;
import cloud.hetzner.api.models.ServersActionsRequestConsoleResponse;
import cloud.hetzner.api.models.Status;
import java.io.IOException;
import java.util.Arrays;

ServersActionsRequestConsoleResponse serversActionsRequestConsoleResponse = new ServersActionsRequestConsoleResponse.Builder(
    new Action.Builder(
        "start_server",
        new Error.Builder(
            "action_failed",
            "Action failed"
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
        "2016-01-30T23:55:00+00:00",
        42,
        100D,
        Arrays.asList(
            new Resource.Builder(
                42,
                "server"
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
        ),
        "2016-01-30T23:55:00+00:00",
        Status.RUNNING
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build(),
    "9MQaTg2VAGI0FIpc10k3UpRXcHj2wQ6x",
    "wss://console.hetzner.cloud/?server_id=1&token=3db32d15-af2f-459c-8bf8-dee1fd05f49c"
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



