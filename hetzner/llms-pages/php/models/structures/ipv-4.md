# Ipv 4

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRklwdjQ

IP address (v4)


# Class Name

`Ipv4`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `dnsPtr` | `?string` | Optional | Reverse DNS PTR entry for the IPv4 address of this Load Balancer | getDnsPtr(): ?string | setDnsPtr(?string dnsPtr): void |
| `ip` | `?string` | Optional | IP address (v4) of this Load Balancer | getIp(): ?string | setIp(?string ip): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\Ipv4Builder;

$ipv4 = Ipv4Builder::init()
    ->dnsPtr('lb1.example.com')
    ->ip('1.2.3.4')
    ->build();
```



