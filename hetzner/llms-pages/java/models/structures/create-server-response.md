# Create Server Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRkNyZWF0ZVNlcnZlclJlc3BvbnNl


# Class Name

`CreateServerResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Action` | [`Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/action.md) | Required | - | Action getAction() | setAction(Action action) |
| `NextActions` | [`List<Action>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/action.md) | Required | - | List<Action> getNextActions() | setNextActions(List<Action> nextActions) |
| `RootPassword` | `String` | Required | Root password when no SSH keys have been specified | String getRootPassword() | setRootPassword(String rootPassword) |
| `Server` | [`Server18`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/server-18.md) | Required | - | Server18 getServer() | setServer(Server18 server) |


# Example

```java
import cloud.hetzner.api.models.Action;
import cloud.hetzner.api.models.CpuTypeEnum;
import cloud.hetzner.api.models.CreateServerResponse;
import cloud.hetzner.api.models.CreatedFrom;
import cloud.hetzner.api.models.Datacenter6;
import cloud.hetzner.api.models.DnsPtr8;
import cloud.hetzner.api.models.Error;
import cloud.hetzner.api.models.Image;
import cloud.hetzner.api.models.Ipv44;
import cloud.hetzner.api.models.Ipv64;
import cloud.hetzner.api.models.Iso2;
import cloud.hetzner.api.models.Location;
import cloud.hetzner.api.models.OsFlavorEnum;
import cloud.hetzner.api.models.PlacementGroupNullable;
import cloud.hetzner.api.models.Price9;
import cloud.hetzner.api.models.PriceHourly8;
import cloud.hetzner.api.models.PriceMonthly10;
import cloud.hetzner.api.models.PrivateNet4;
import cloud.hetzner.api.models.Protection;
import cloud.hetzner.api.models.Protection20;
import cloud.hetzner.api.models.PublicNet4;
import cloud.hetzner.api.models.Resource;
import cloud.hetzner.api.models.Server18;
import cloud.hetzner.api.models.ServerPublicNetFirewall;
import cloud.hetzner.api.models.ServerType1;
import cloud.hetzner.api.models.ServerTypes;
import cloud.hetzner.api.models.Status24Enum;
import cloud.hetzner.api.models.Status72Enum;
import cloud.hetzner.api.models.Status73Enum;
import cloud.hetzner.api.models.StatusEnum;
import cloud.hetzner.api.models.StorageTypeEnum;
import cloud.hetzner.api.models.Type22Enum;
import cloud.hetzner.api.models.Type26Enum;
import java.util.Arrays;
import java.util.LinkedHashMap;

CreateServerResponse createServerResponse = new CreateServerResponse.Builder(
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
    "YItygq1v3GYjjMomLaKc",
    new Server18.Builder(
        "22-02",
        "2016-01-30T23:55:00+00:00",
        new Datacenter6.Builder(
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
        42,
        new Image.Builder(
            null,
            "2016-01-30T23:55:00+00:00",
            new CreatedFrom.Builder(
                1,
                "Server"
            )
            .build(),
            null,
            "2018-02-28T00:00:00+00:00",
            "Ubuntu 20.04 Standard 64 bit",
            10D,
            42,
            2.3D,
            new LinkedHashMap<String, String>() {{
                put("key0", "labels4");
            }},
            "ubuntu-20.04",
            OsFlavorEnum.UBUNTU,
            "20.04",
            new Protection.Builder(
                false
            )
            .build(),
            Status24Enum.UNAVAILABLE,
            Type22Enum.SNAPSHOT
        )
        .rapidDeploy(false)
        .build(),
        654321D,
        123456D,
        new Iso2.Builder(
            "2018-02-28T00:00:00+00:00",
            "FreeBSD 11.0 x64",
            42,
            "FreeBSD-11.0-RELEASE-amd64-dvd1",
            Type26Enum.ENUM_PUBLIC
        )
        .build(),
        new LinkedHashMap<String, String>() {{
            put("key0", "labels0");
            put("key1", "labels9");
        }},
        false,
        "my-resource",
        123456D,
        50D,
        Arrays.asList(
            new PrivateNet4.Builder()
                .aliasIps(Arrays.asList(
                    "alias_ips4"
                ))
                .ip("10.0.0.2")
                .macAddress("86:00:ff:2a:7d:e1")
                .network(4711)
                .build()
        ),
        new Protection20.Builder(
            false,
            false
        )
        .build(),
        new PublicNet4.Builder(
            Arrays.asList(
                478
            ),
            new Ipv44.Builder(
                false,
                "server01.example.com",
                "1.2.3.4"
            )
            .id(42)
            .build(),
            new Ipv64.Builder(
                false,
                Arrays.asList(
                    new DnsPtr8.Builder(
                        "server.example.com",
                        "2001:db8::1"
                    )
                    .build()
                ),
                "2001:db8::/64"
            )
            .id(42)
            .build()
        )
        .firewalls(Arrays.asList(
                new ServerPublicNetFirewall.Builder()
                    .id(250)
                    .status(Status72Enum.APPLIED)
                    .build(),
                new ServerPublicNetFirewall.Builder()
                    .id(250)
                    .status(Status72Enum.APPLIED)
                    .build()
            ))
        .build(),
        false,
        new ServerType1.Builder(
            1D,
            CpuTypeEnum.SHARED,
            false,
            "CX11",
            25D,
            1,
            1D,
            "cx11",
            Arrays.asList(
                new Price9.Builder(
                    "fsn1",
                    new PriceHourly8.Builder(
                        "1.1900000000000000",
                        "1.0000000000"
                    )
                    .build(),
                    new PriceMonthly10.Builder(
                        "1.1900000000000000",
                        "1.0000000000"
                    )
                    .build()
                )
                .build()
            ),
            StorageTypeEnum.LOCAL
        )
        .build(),
        Status73Enum.STARTING
    )
    .loadBalancers(Arrays.asList(
            144,
            143,
            142
        ))
    .placementGroup(new PlacementGroupNullable.Builder(
            "created8",
            236,
            new LinkedHashMap<String, String>() {{
                put("key0", "labels4");
            }},
            "name8",
            Arrays.asList(
                251,
                252,
                253
            ),
            "type2"
        )
        .build())
    .volumes(Arrays.asList(
            91,
            92
        ))
    .build()
)
.build();
```



