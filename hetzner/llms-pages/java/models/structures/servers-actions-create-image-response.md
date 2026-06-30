# Servers Actions Create Image Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMENyZWF0ZSUyNTIwSW1hZ2UlMjUyMFJlc3BvbnNl


# Class Name

`ServersActionsCreateImageResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Action` | [`Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/action.md) | Optional | - | Action getAction() | setAction(Action action) |
| `Image` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/image.md) | Optional | - | Image getImage() | setImage(Image image) |


# Example

```java
import cloud.hetzner.api.models.Action;
import cloud.hetzner.api.models.CreatedFrom;
import cloud.hetzner.api.models.Error;
import cloud.hetzner.api.models.Image;
import cloud.hetzner.api.models.OsFlavorEnum;
import cloud.hetzner.api.models.Protection;
import cloud.hetzner.api.models.Resource;
import cloud.hetzner.api.models.ServersActionsCreateImageResponse;
import cloud.hetzner.api.models.Status24Enum;
import cloud.hetzner.api.models.StatusEnum;
import cloud.hetzner.api.models.Type22Enum;
import java.util.Arrays;
import java.util.LinkedHashMap;

ServersActionsCreateImageResponse serversActionsCreateImageResponse = new ServersActionsCreateImageResponse.Builder()
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
    .image(new Image.Builder(
        186,
        "created6",
        new CreatedFrom.Builder(
            60,
            "name6"
        )
        .build(),
        "deleted4",
        "deprecated8",
        "description6",
        244.18D,
        128,
        141.34D,
        new LinkedHashMap<String, String>() {{
            put("key0", "labels4");
        }},
        "name6",
        OsFlavorEnum.DEBIAN,
        "os_version4",
        new Protection.Builder(
            false
        )
        .build(),
        Status24Enum.UNAVAILABLE,
        Type22Enum.APP
    )
    .rapidDeploy(false)
    .build())
    .build();
```



