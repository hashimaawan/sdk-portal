# Floating Ips Actions Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkZsb2F0aW5nJTI1MjBJcHMlMjUyMEFjdGlvbnMlMjUyMFJlc3BvbnNl


# Class Name

`FloatingIpsActionsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Actions` | [`List<Action>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/action.md) | Required | - | List<Action> getActions() | setActions(List<Action> actions) |


# Example

```java
import cloud.hetzner.api.models.Action;
import cloud.hetzner.api.models.Error;
import cloud.hetzner.api.models.FloatingIpsActionsResponse;
import cloud.hetzner.api.models.Resource;
import cloud.hetzner.api.models.StatusEnum;
import java.util.Arrays;

FloatingIpsActionsResponse floatingIpsActionsResponse = new FloatingIpsActionsResponse.Builder(
    Arrays.asList(
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
            StatusEnum.SUCCESS
        )
        .build()
    )
)
.build();
```



