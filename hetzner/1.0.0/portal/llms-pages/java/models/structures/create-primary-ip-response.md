# Create Primary IP Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkNyZWF0ZVByaW1hcnlJUFJlc3BvbnNl


# Class Name

`CreatePrimaryIPResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Action` | [`Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/action.md) | Optional | - | Action getAction() | setAction(Action action) |
| `PrimaryIp` | [`PrimaryIP1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/primary-ip-1.md) | Required | - | PrimaryIP1 getPrimaryIp() | setPrimaryIp(PrimaryIP1 primaryIp) |


# Example

```java
import cloud.hetzner.api.models.Action;
import cloud.hetzner.api.models.CreatePrimaryIPResponse;
import cloud.hetzner.api.models.Datacenter2;
import cloud.hetzner.api.models.DnsPtr;
import cloud.hetzner.api.models.Error;
import cloud.hetzner.api.models.Location;
import cloud.hetzner.api.models.PrimaryIP1;
import cloud.hetzner.api.models.Protection;
import cloud.hetzner.api.models.Resource;
import cloud.hetzner.api.models.ServerTypes;
import cloud.hetzner.api.models.StatusEnum;
import cloud.hetzner.api.models.Type50Enum;
import java.util.Arrays;
import java.util.LinkedHashMap;

CreatePrimaryIPResponse createPrimaryIPResponse = new CreatePrimaryIPResponse.Builder(
    new PrimaryIP1.Builder(
        17,
        "server",
        true,
        false,
        "2016-01-30T23:55:00+00:00",
        new Datacenter2.Builder(
            "Falkenstein DC Park 8",
            42,
            new Location.Builder(
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
            "fsn1-dc8",
            new ServerTypes.Builder(
                Arrays.asList(
                    1D,
                    2D,
                    3D
                ),
                Arrays.asList(
                    1D,
                    2D,
                    3D
                ),
                Arrays.asList(
                    1D,
                    2D,
                    3D
                )
            )
            .build()
        )
        .build(),
        Arrays.asList(
            new DnsPtr.Builder(
                "server.example.com",
                "2001:db8::1"
            )
            .build()
        ),
        42,
        "131.232.99.1",
        new LinkedHashMap<String, String>() {{
            put("key0", "labels2");
            put("key1", "labels1");
        }},
        "my-resource",
        new Protection.Builder(
            false
        )
        .build(),
        Type50Enum.IPV4
    )
    .build()
)
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



