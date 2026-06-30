# Primary IP 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRlByaW1hcnlJUDE


# Class Name

`PrimaryIP1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AssigneeId` | `Integer` | Required | ID of the resource the Primary IP is assigned to, null if it is not assigned at all | Integer getAssigneeId() | setAssigneeId(Integer assigneeId) |
| `AssigneeType` | `String` | Required, Constant | Resource type the Primary IP can be assigned to<br><br>**Value**: `"server"` | String getAssigneeType() | setAssigneeType(String assigneeType) |
| `AutoDelete` | `boolean` | Required | Delete this Primary IP when the resource it is assigned to is deleted | boolean getAutoDelete() | setAutoDelete(boolean autoDelete) |
| `Blocked` | `boolean` | Required | Whether the IP is blocked | boolean getBlocked() | setBlocked(boolean blocked) |
| `Created` | `String` | Required | Point in time when the Resource was created (in ISO-8601 format) | String getCreated() | setCreated(String created) |
| `Datacenter` | [`Datacenter2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/datacenter-2.md) | Required | Datacenter this Primary IP is located at | Datacenter2 getDatacenter() | setDatacenter(Datacenter2 datacenter) |
| `DnsPtr` | [`List<DnsPtr>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/dns-ptr.md) | Required | Array of reverse DNS entries | List<DnsPtr> getDnsPtr() | setDnsPtr(List<DnsPtr> dnsPtr) |
| `Id` | `int` | Required | ID of the Resource | int getId() | setId(int id) |
| `Ip` | `String` | Required | IP address | String getIp() | setIp(String ip) |
| `Labels` | `Map<String, String>` | Required | User-defined labels (key-value pairs) | Map<String, String> getLabels() | setLabels(Map<String, String> labels) |
| `Name` | `String` | Required | Name of the Resource. Must be unique per Project. | String getName() | setName(String name) |
| `Protection` | [`Protection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/protection.md) | Required | Protection configuration for the Resource | Protection getProtection() | setProtection(Protection protection) |
| `Type` | [`Type50Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/enumerations/type-50.md) | Required | Type of the Primary IP | Type50Enum getType() | setType(Type50Enum type) |


# Example

```java
import cloud.hetzner.api.models.Datacenter2;
import cloud.hetzner.api.models.DnsPtr;
import cloud.hetzner.api.models.Location;
import cloud.hetzner.api.models.PrimaryIP1;
import cloud.hetzner.api.models.Protection;
import cloud.hetzner.api.models.ServerTypes;
import cloud.hetzner.api.models.Type50Enum;
import java.util.Arrays;
import java.util.LinkedHashMap;

PrimaryIP1 primaryIP1 = new PrimaryIP1.Builder(
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
        put("key0", "labels4");
        put("key1", "labels3");
    }},
    "my-resource",
    new Protection.Builder(
        false
    )
    .build(),
    Type50Enum.IPV4
)
.build();
```



