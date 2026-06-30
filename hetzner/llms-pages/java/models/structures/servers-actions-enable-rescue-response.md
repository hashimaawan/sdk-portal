# Servers Actions Enable Rescue Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMEVuYWJsZSUyNTIwUmVzY3VlJTI1MjBSZXNwb25zZQ


# Class Name

`ServersActionsEnableRescueResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Action` | [`Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/action.md) | Optional | - | Action getAction() | setAction(Action action) |
| `RootPassword` | `String` | Optional | Password that will be set for this Server once the Action succeeds | String getRootPassword() | setRootPassword(String rootPassword) |


# Example

```java
import cloud.hetzner.api.models.Action;
import cloud.hetzner.api.models.Error;
import cloud.hetzner.api.models.Resource;
import cloud.hetzner.api.models.ServersActionsEnableRescueResponse;
import cloud.hetzner.api.models.StatusEnum;
import java.util.Arrays;

ServersActionsEnableRescueResponse serversActionsEnableRescueResponse = new ServersActionsEnableRescueResponse.Builder()
    .action(new Action.Builder(
        "command6",
        new Error.Builder(
            "code2",
            "message4"
        )
        .build(),
        "finished0",
        238,
        143.26D,
        Arrays.asList(
            new Resource.Builder(
                198,
                "type0"
            )
            .build(),
            new Resource.Builder(
                198,
                "type0"
            )
            .build(),
            new Resource.Builder(
                198,
                "type0"
            )
            .build()
        ),
        "started8",
        StatusEnum.RUNNING
    )
    .build())
    .rootPassword("zCWbFhnu950dUTko5f40")
    .build();
```



