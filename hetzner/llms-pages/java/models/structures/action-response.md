# Action Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRkFjdGlvblJlc3BvbnNl


# Class Name

`ActionResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Action` | [`Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/action.md) | Required | - | Action getAction() | setAction(Action action) |


# Example

```java
import cloud.hetzner.api.models.Action;
import cloud.hetzner.api.models.ActionResponse;
import cloud.hetzner.api.models.Error;
import cloud.hetzner.api.models.Resource;
import cloud.hetzner.api.models.StatusEnum;
import java.util.Arrays;

ActionResponse actionResponse = new ActionResponse.Builder(
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
    .build()
)
.build();
```



