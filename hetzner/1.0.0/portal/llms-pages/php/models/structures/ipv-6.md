# Ipv 6

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRklwdjY

IP address (v6)

*This model accepts additional fields of type array.*


# Class Name

`Ipv6`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `dnsPtr` | `?string` | Optional | Reverse DNS PTR entry for the IPv6 address of this Load Balancer | getDnsPtr(): ?string | setDnsPtr(?string dnsPtr): void |
| `ip` | `?string` | Optional | IP address (v6) of this Load Balancer | getIp(): ?string | setIp(?string ip): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\Ipv6Builder;
use HetznerCloudApiLib\ApiHelper;

$ipv6 = Ipv6Builder::init()
    ->dnsPtr('lb1.example.com')
    ->ip('2001:db8::1')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



