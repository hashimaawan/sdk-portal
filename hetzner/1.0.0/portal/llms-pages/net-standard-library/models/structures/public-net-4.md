# Public Net 4

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlB1YmxpY05ldDQ

Public network information. The Server's IPv4 address can be found in `public_net->ipv4->ip`


# Class Name

`PublicNet4`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Firewalls` | [`List<ServerPublicNetFirewall>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/server-public-net-firewall.md) | Optional | Firewalls applied to the public network interface of this Server |
| `FloatingIps` | `List<int>` | Required | IDs of Floating IPs assigned to this Server |
| `Ipv4` | [`Ipv44`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/ipv-44.md) | Required | IP address (v4) and its reverse DNS entry of this Server |
| `Ipv6` | [`Ipv64`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/ipv-64.md) | Required | IPv6 network assigned to this Server and its reverse DNS entry |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;
using System.Collections.Generic;

PublicNet4 publicNet4 = new PublicNet4
{
    FloatingIps = new List<int>
    {
        478,
    },
    Ipv4 = new Ipv44
    {
        Blocked = false,
        DnsPtr = "server01.example.com",
        Ip = "1.2.3.4",
        Id = 42,
    },
    Ipv6 = new Ipv64
    {
        Blocked = false,
        DnsPtr = new List<DnsPtr8>
        {
            new DnsPtr8
            {
                DnsPtr = "server.example.com",
                Ip = "2001:db8::1",
            },
        },
        Ip = "2001:db8::/64",
        Id = 42,
    },
    Firewalls = new List<ServerPublicNetFirewall>
    {
        new ServerPublicNetFirewall
        {
            Id = 250,
            Status = Status72Enum.Applied,
        },
    },
};
```



