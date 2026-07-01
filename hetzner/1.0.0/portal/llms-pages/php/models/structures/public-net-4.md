# Public Net 4

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlB1YmxpY05ldDQ

Public network information. The Server's IPv4 address can be found in `public_net->ipv4->ip`

*This model accepts additional fields of type array.*


# Class Name

`PublicNet4`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `firewalls` | [`?(ServerPublicNetFirewall[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/server-public-net-firewall.md) | Optional | Firewalls applied to the public network interface of this Server | getFirewalls(): ?array | setFirewalls(?array firewalls): void |
| `floatingIps` | `int[]` | Required | IDs of Floating IPs assigned to this Server | getFloatingIps(): array | setFloatingIps(array floatingIps): void |
| `ipv4` | [`?Ipv44`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/ipv-44.md) | Required | IP address (v4) and its reverse DNS entry of this Server | getIpv4(): ?Ipv44 | setIpv4(?Ipv44 ipv4): void |
| `ipv6` | [`?Ipv64`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/ipv-64.md) | Required | IPv6 network assigned to this Server and its reverse DNS entry | getIpv6(): ?Ipv64 | setIpv6(?Ipv64 ipv6): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\PublicNet4Builder;
use HetznerCloudApiLib\Models\Builders\ServerPublicNetFirewallBuilder;
use HetznerCloudApiLib\Models\Status72;
use HetznerCloudApiLib\ApiHelper;
use HetznerCloudApiLib\Models\Builders\Ipv44Builder;
use HetznerCloudApiLib\Models\Builders\Ipv64Builder;
use HetznerCloudApiLib\Models\Builders\DnsPtr8Builder;

$publicNet4 = PublicNet4Builder::init(
    [
        478
    ]
)
    ->firewalls(
        [
            ServerPublicNetFirewallBuilder::init()
                ->id(250)
                ->status(Status72::APPLIED)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
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
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
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
                    )
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                ]
            )
            ->id(42)
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



