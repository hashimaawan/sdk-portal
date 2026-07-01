# Server 18

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlNlcnZlcjE4


# Class Name

`Server18`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `BackupWindow` | `String` | Required | Time window (UTC) in which the backup will run, or null if the backups are not enabled | String getBackupWindow() | setBackupWindow(String backupWindow) |
| `Created` | `String` | Required | Point in time when the Resource was created (in ISO-8601 format) | String getCreated() | setCreated(String created) |
| `Datacenter` | [`Datacenter6`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/datacenter-6.md) | Required | Datacenter this Resource is located at | Datacenter6 getDatacenter() | setDatacenter(Datacenter6 datacenter) |
| `Id` | `int` | Required | ID of the Resource | int getId() | setId(int id) |
| `Image` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/image.md) | Required | - | Image getImage() | setImage(Image image) |
| `IncludedTraffic` | `Double` | Required | Free Traffic for the current billing period in bytes | Double getIncludedTraffic() | setIncludedTraffic(Double includedTraffic) |
| `IngoingTraffic` | `Double` | Required | Inbound Traffic for the current billing period in bytes | Double getIngoingTraffic() | setIngoingTraffic(Double ingoingTraffic) |
| `Iso` | [`Iso2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/iso-2.md) | Required | ISO Image that is attached to this Server. Null if no ISO is attached. | Iso2 getIso() | setIso(Iso2 iso) |
| `Labels` | `Map<String, String>` | Required | User-defined labels (key-value pairs) | Map<String, String> getLabels() | setLabels(Map<String, String> labels) |
| `LoadBalancers` | `List<Integer>` | Optional | - | List<Integer> getLoadBalancers() | setLoadBalancers(List<Integer> loadBalancers) |
| `Locked` | `boolean` | Required | True if Server has been locked and is not available to user | boolean getLocked() | setLocked(boolean locked) |
| `Name` | `String` | Required | Name of the Server (must be unique per Project and a valid hostname as per RFC 1123) | String getName() | setName(String name) |
| `OutgoingTraffic` | `Double` | Required | Outbound Traffic for the current billing period in bytes | Double getOutgoingTraffic() | setOutgoingTraffic(Double outgoingTraffic) |
| `PlacementGroup` | [`PlacementGroupNullable`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/placement-group-nullable.md) | Optional | - | PlacementGroupNullable getPlacementGroup() | setPlacementGroup(PlacementGroupNullable placementGroup) |
| `PrimaryDiskSize` | `double` | Required | Size of the primary Disk | double getPrimaryDiskSize() | setPrimaryDiskSize(double primaryDiskSize) |
| `PrivateNet` | [`List<PrivateNet4>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/private-net-4.md) | Required | Private networks information | List<PrivateNet4> getPrivateNet() | setPrivateNet(List<PrivateNet4> privateNet) |
| `Protection` | [`Protection20`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/protection-20.md) | Required | Protection configuration for the Server | Protection20 getProtection() | setProtection(Protection20 protection) |
| `PublicNet` | [`PublicNet4`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/public-net-4.md) | Required | Public network information. The Server's IPv4 address can be found in `public_net->ipv4->ip` | PublicNet4 getPublicNet() | setPublicNet(PublicNet4 publicNet) |
| `RescueEnabled` | `boolean` | Required | True if rescue mode is enabled. Server will then boot into rescue system on next reboot | boolean getRescueEnabled() | setRescueEnabled(boolean rescueEnabled) |
| `ServerType` | [`ServerType1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/server-type-1.md) | Required | Type of Server - determines how much ram, disk and cpu a Server has | ServerType1 getServerType() | setServerType(ServerType1 serverType) |
| `Status` | [`Status73Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/enumerations/status-73.md) | Required | Status of the Server | Status73Enum getStatus() | setStatus(Status73Enum status) |
| `Volumes` | `List<Integer>` | Optional | IDs of Volumes assigned to this Server | List<Integer> getVolumes() | setVolumes(List<Integer> volumes) |


# Example

```java
import cloud.hetzner.api.models.CpuTypeEnum;
import cloud.hetzner.api.models.CreatedFrom;
import cloud.hetzner.api.models.Datacenter6;
import cloud.hetzner.api.models.DnsPtr8;
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
import cloud.hetzner.api.models.Server18;
import cloud.hetzner.api.models.ServerPublicNetFirewall;
import cloud.hetzner.api.models.ServerType1;
import cloud.hetzner.api.models.ServerTypes;
import cloud.hetzner.api.models.Status24Enum;
import cloud.hetzner.api.models.Status72Enum;
import cloud.hetzner.api.models.Status73Enum;
import cloud.hetzner.api.models.StorageTypeEnum;
import cloud.hetzner.api.models.Type22Enum;
import cloud.hetzner.api.models.Type26Enum;
import java.util.Arrays;
import java.util.LinkedHashMap;

Server18 server18 = new Server18.Builder(
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
        put("key0", "labels4");
        put("key1", "labels3");
        put("key2", "labels2");
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
    Status73Enum.RUNNING
)
.loadBalancers(Arrays.asList(
        248
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
        199,
        200,
        201
    ))
.build();
```



