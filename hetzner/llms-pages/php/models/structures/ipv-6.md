# Ipv 6

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRklwdjY

IP address (v6)


# Class Name

`Ipv6`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `dnsPtr` | `?string` | Optional | Reverse DNS PTR entry for the IPv6 address of this Load Balancer | getDnsPtr(): ?string | setDnsPtr(?string dnsPtr): void |
| `ip` | `?string` | Optional | IP address (v6) of this Load Balancer | getIp(): ?string | setIp(?string ip): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\Ipv6Builder;

$ipv6 = Ipv6Builder::init()
    ->dnsPtr('lb1.example.com')
    ->ip('2001:db8::1')
    ->build();
```



