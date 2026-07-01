# Ipv 64

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRklwdjY0

IPv6 network assigned to this Server and its reverse DNS entry


# Class Name

`Ipv64`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `blocked` | `bool` | Required | If the IP is blocked by our anti abuse dept | getBlocked(): bool | setBlocked(bool blocked): void |
| `dnsPtr` | [`?(DnsPtr8[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/dns-ptr-8.md) | Required | Reverse DNS PTR entries for the IPv6 addresses of this Server, `null` by default | getDnsPtr(): ?array | setDnsPtr(?array dnsPtr): void |
| `id` | `?int` | Optional | ID of the Resource | getId(): ?int | setId(?int id): void |
| `ip` | `string` | Required | IP address (v6) of this Server | getIp(): string | setIp(string ip): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\Ipv64Builder;
use HetznerCloudAPILib\Models\Builders\DnsPtr8Builder;

$ipv64 = Ipv64Builder::init(
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
    ->build();
```



