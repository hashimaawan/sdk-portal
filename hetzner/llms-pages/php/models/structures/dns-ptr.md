# Dns Ptr

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRkRuc1B0cg


# Class Name

`DnsPtr`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `dnsPtr` | `string` | Required | DNS pointer for the specific IP address | getDnsPtr(): string | setDnsPtr(string dnsPtr): void |
| `ip` | `string` | Required | Single IPv4 or IPv6 address | getIp(): string | setIp(string ip): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\DnsPtrBuilder;

$dnsPtr = DnsPtrBuilder::init(
    'server.example.com',
    '2001:db8::1'
)->build();
```



