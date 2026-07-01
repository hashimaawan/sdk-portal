# Servers Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMFJlc3BvbnNlMQ


# Class Name

`ServersResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Action` | [`Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/action.md) | Optional | - | Action getAction() | setAction(Action action) |


# Example

```java
import cloud.hetzner.api.models.Action;
import cloud.hetzner.api.models.Error;
import cloud.hetzner.api.models.Resource;
import cloud.hetzner.api.models.ServersResponse1;
import cloud.hetzner.api.models.StatusEnum;
import java.util.Arrays;

ServersResponse1 serversResponse1 = new ServersResponse1.Builder()
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
    .build();
```



