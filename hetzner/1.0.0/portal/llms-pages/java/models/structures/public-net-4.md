# Public Net 4

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlB1YmxpY05ldDQ

Public network information. The Server's IPv4 address can be found in `public_net->ipv4->ip`


# Class Name

`PublicNet4`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Firewalls` | [`List<ServerPublicNetFirewall>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/server-public-net-firewall.md) | Optional | Firewalls applied to the public network interface of this Server | List<ServerPublicNetFirewall> getFirewalls() | setFirewalls(List<ServerPublicNetFirewall> firewalls) |
| `FloatingIps` | `List<Integer>` | Required | IDs of Floating IPs assigned to this Server | List<Integer> getFloatingIps() | setFloatingIps(List<Integer> floatingIps) |
| `Ipv4` | [`Ipv44`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/ipv-44.md) | Required | IP address (v4) and its reverse DNS entry of this Server | Ipv44 getIpv4() | setIpv4(Ipv44 ipv4) |
| `Ipv6` | [`Ipv64`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/ipv-64.md) | Required | IPv6 network assigned to this Server and its reverse DNS entry | Ipv64 getIpv6() | setIpv6(Ipv64 ipv6) |


# Example

```java
import cloud.hetzner.api.models.DnsPtr8;
import cloud.hetzner.api.models.Ipv44;
import cloud.hetzner.api.models.Ipv64;
import cloud.hetzner.api.models.PublicNet4;
import cloud.hetzner.api.models.ServerPublicNetFirewall;
import cloud.hetzner.api.models.Status72Enum;
import java.util.Arrays;

PublicNet4 publicNet4 = new PublicNet4.Builder(
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
            .build()
    ))
.build();
```



