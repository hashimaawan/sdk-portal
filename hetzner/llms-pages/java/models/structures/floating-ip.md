# Floating Ip

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRkZsb2F0aW5nSXA


# Class Name

`FloatingIp`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Blocked` | `boolean` | Required | Whether the IP is blocked | boolean getBlocked() | setBlocked(boolean blocked) |
| `Created` | `String` | Required | Point in time when the Resource was created (in ISO-8601 format) | String getCreated() | setCreated(String created) |
| `Description` | `String` | Required | Description of the Resource | String getDescription() | setDescription(String description) |
| `DnsPtr` | [`List<DnsPtr>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/dns-ptr.md) | Required | Array of reverse DNS entries | List<DnsPtr> getDnsPtr() | setDnsPtr(List<DnsPtr> dnsPtr) |
| `HomeLocation` | [`HomeLocation`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/home-location.md) | Required | Location the Floating IP was created in. Routing is optimized for this Location. | HomeLocation getHomeLocation() | setHomeLocation(HomeLocation homeLocation) |
| `Id` | `int` | Required | ID of the Resource | int getId() | setId(int id) |
| `Ip` | `String` | Required | IP address | String getIp() | setIp(String ip) |
| `Labels` | `Map<String, String>` | Required | User-defined labels (key-value pairs) | Map<String, String> getLabels() | setLabels(Map<String, String> labels) |
| `Name` | `String` | Required | Name of the Resource. Must be unique per Project. | String getName() | setName(String name) |
| `Protection` | [`Protection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/protection.md) | Required | Protection configuration for the Resource | Protection getProtection() | setProtection(Protection protection) |
| `Server` | `Integer` | Required | ID of the Server the Floating IP is assigned to, null if it is not assigned at all | Integer getServer() | setServer(Integer server) |
| `Type` | [`Type16Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/enumerations/type-16.md) | Required | Type of the Floating IP | Type16Enum getType() | setType(Type16Enum type) |


# Example

```java
import cloud.hetzner.api.models.DnsPtr;
import cloud.hetzner.api.models.FloatingIp;
import cloud.hetzner.api.models.HomeLocation;
import cloud.hetzner.api.models.Protection;
import cloud.hetzner.api.models.Type16Enum;
import java.util.Arrays;
import java.util.LinkedHashMap;

FloatingIp floatingIp = new FloatingIp.Builder(
    false,
    "2016-01-30T23:55:00+00:00",
    "this describes my resource",
    Arrays.asList(
        new DnsPtr.Builder(
            "server.example.com",
            "2001:db8::1"
        )
        .build()
    ),
    new HomeLocation.Builder(
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
    42,
    "131.232.99.1",
    new LinkedHashMap<String, String>() {{
        put("key0", "labels6");
    }},
    "my-resource",
    new Protection.Builder(
        false
    )
    .build(),
    42,
    Type16Enum.IPV4
)
.build();
```



