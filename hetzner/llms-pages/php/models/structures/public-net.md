# Public Net

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRlB1YmxpY05ldA

Public network information


# Class Name

`PublicNet`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `enabled` | `bool` | Required | Public Interface enabled or not | getEnabled(): bool | setEnabled(bool enabled): void |
| `ipv4` | [`Ipv4`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/ipv-4.md) | Required | IP address (v4) | getIpv4(): Ipv4 | setIpv4(Ipv4 ipv4): void |
| `ipv6` | [`Ipv6`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/ipv-6.md) | Required | IP address (v6) | getIpv6(): Ipv6 | setIpv6(Ipv6 ipv6): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\PublicNetBuilder;
use HetznerCloudAPILib\Models\Builders\Ipv4Builder;
use HetznerCloudAPILib\Models\Builders\Ipv6Builder;

$publicNet = PublicNetBuilder::init(
    false,
    Ipv4Builder::init()
        ->dnsPtr('lb1.example.com')
        ->ip('1.2.3.4')
        ->build(),
    Ipv6Builder::init()
        ->dnsPtr('lb1.example.com')
        ->ip('2001:db8::1')
        ->build()
)->build();
```



