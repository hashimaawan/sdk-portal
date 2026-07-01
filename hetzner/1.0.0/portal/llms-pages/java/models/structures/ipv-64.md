# Ipv 64

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRklwdjY0

IPv6 network assigned to this Server and its reverse DNS entry


# Class Name

`Ipv64`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Blocked` | `boolean` | Required | If the IP is blocked by our anti abuse dept | boolean getBlocked() | setBlocked(boolean blocked) |
| `DnsPtr` | [`List<DnsPtr8>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/dns-ptr-8.md) | Required | Reverse DNS PTR entries for the IPv6 addresses of this Server, `null` by default | List<DnsPtr8> getDnsPtr() | setDnsPtr(List<DnsPtr8> dnsPtr) |
| `Id` | `Integer` | Optional | ID of the Resource | Integer getId() | setId(Integer id) |
| `Ip` | `String` | Required | IP address (v6) of this Server | String getIp() | setIp(String ip) |


# Example

```java
import cloud.hetzner.api.models.DnsPtr8;
import cloud.hetzner.api.models.Ipv64;
import java.util.Arrays;

Ipv64 ipv64 = new Ipv64.Builder(
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
.build();
```



