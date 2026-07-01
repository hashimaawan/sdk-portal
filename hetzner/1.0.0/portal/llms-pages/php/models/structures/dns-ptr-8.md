# Dns Ptr 8

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkRuc1B0cjg


# Class Name

`DnsPtr8`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `dnsPtr` | `string` | Required | DNS pointer for the specific IP address | getDnsPtr(): string | setDnsPtr(string dnsPtr): void |
| `ip` | `string` | Required | Single IPv6 address of this Server for which the reverse DNS entry has been set up | getIp(): string | setIp(string ip): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\DnsPtr8Builder;

$dnsPtr8 = DnsPtr8Builder::init(
    'server.example.com',
    '2001:db8::1'
)->build();
```



