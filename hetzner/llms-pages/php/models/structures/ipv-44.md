# Ipv 44

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRklwdjQ0

IP address (v4) and its reverse DNS entry of this Server


# Class Name

`Ipv44`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `blocked` | `bool` | Required | If the IP is blocked by our anti abuse dept | getBlocked(): bool | setBlocked(bool blocked): void |
| `dnsPtr` | `string` | Required | Reverse DNS PTR entry for the IPv4 addresses of this Server | getDnsPtr(): string | setDnsPtr(string dnsPtr): void |
| `id` | `?int` | Optional | ID of the Resource | getId(): ?int | setId(?int id): void |
| `ip` | `string` | Required | IP address (v4) of this Server | getIp(): string | setIp(string ip): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\Ipv44Builder;

$ipv44 = Ipv44Builder::init(
    false,
    'server01.example.com',
    '1.2.3.4'
)
    ->id(42)
    ->build();
```



