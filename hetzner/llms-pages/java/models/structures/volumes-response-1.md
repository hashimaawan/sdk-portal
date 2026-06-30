# Volumes Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRlZvbHVtZXMlMjUyMFJlc3BvbnNlMQ


# Class Name

`VolumesResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Action` | [`Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/action.md) | Required | - | Action getAction() | setAction(Action action) |
| `NextActions` | [`List<Action>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/action.md) | Required | - | List<Action> getNextActions() | setNextActions(List<Action> nextActions) |
| `Volume` | [`Volume1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/volume-1.md) | Required | - | Volume1 getVolume() | setVolume(Volume1 volume) |


# Example

```java
import cloud.hetzner.api.models.Action;
import cloud.hetzner.api.models.Error;
import cloud.hetzner.api.models.Location16;
import cloud.hetzner.api.models.Protection;
import cloud.hetzner.api.models.Resource;
import cloud.hetzner.api.models.Status113Enum;
import cloud.hetzner.api.models.StatusEnum;
import cloud.hetzner.api.models.Volume1;
import cloud.hetzner.api.models.VolumesResponse1;
import java.util.Arrays;
import java.util.LinkedHashMap;

VolumesResponse1 volumesResponse1 = new VolumesResponse1.Builder(
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
    ),
    new Volume1.Builder(
        "2016-01-30T23:55:00+00:00",
        "xfs",
        42,
        new LinkedHashMap<String, String>() {{
            put("key0", "labels8");
            put("key1", "labels9");
            put("key2", "labels0");
        }},
        "/dev/disk/by-id/scsi-0HC_Volume_4711",
        new Location16.Builder(
            "Falkenstein",
            "DE",
            "Falkenstein DC Park 1",
            1D,
            50.47612D,
            12.370071D,
            "fsn1",
            "eu-central"
        )
        .build(),
        "my-resource",
        new Protection.Builder(
            false
        )
        .build(),
        12,
        42D,
        Status113Enum.AVAILABLE
    )
    .build()
)
.build();
```



