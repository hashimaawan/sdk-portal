# Public Net 4

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRlB1YmxpY05ldDQ

Public network information. The Server's IPv4 address can be found in `public_net->ipv4->ip`


# Class Name

`PublicNet4`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `firewalls` | [`?(ServerPublicNetFirewall[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/server-public-net-firewall.md) | Optional | Firewalls applied to the public network interface of this Server | getFirewalls(): ?array | setFirewalls(?array firewalls): void |
| `floatingIps` | `int[]` | Required | IDs of Floating IPs assigned to this Server | getFloatingIps(): array | setFloatingIps(array floatingIps): void |
| `ipv4` | [`?Ipv44`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/ipv-44.md) | Required | IP address (v4) and its reverse DNS entry of this Server | getIpv4(): ?Ipv44 | setIpv4(?Ipv44 ipv4): void |
| `ipv6` | [`?Ipv64`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/ipv-64.md) | Required | IPv6 network assigned to this Server and its reverse DNS entry | getIpv6(): ?Ipv64 | setIpv6(?Ipv64 ipv6): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\PublicNet4Builder;
use HetznerCloudAPILib\Models\Builders\ServerPublicNetFirewallBuilder;
use HetznerCloudAPILib\Models\Status72Enum;
use HetznerCloudAPILib\Models\Builders\Ipv44Builder;
use HetznerCloudAPILib\Models\Builders\Ipv64Builder;
use HetznerCloudAPILib\Models\Builders\DnsPtr8Builder;

$publicNet4 = PublicNet4Builder::init(
    [
        478
    ]
)
    ->firewalls(
        [
            ServerPublicNetFirewallBuilder::init()
                ->id(250)
                ->status(Status72Enum::APPLIED)
                ->build()
        ]
    )
    ->ipv4(
        Ipv44Builder::init(
            false,
            'server01.example.com',
            '1.2.3.4'
        )
            ->id(42)
            ->build()
    )
    ->ipv6(
        Ipv64Builder::init(
            false,
            '2001:db8::/64'
        )
            ->dnsPtr(
                [
                    DnsPtr8Builder::init(
                        'server.example.com',
                        '2001:db8::1'
                    )->build()
                ]
            )
            ->id(42)
            ->build()
    )
    ->build();
```



