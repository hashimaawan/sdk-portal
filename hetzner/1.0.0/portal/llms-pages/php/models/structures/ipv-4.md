# Ipv 4

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRklwdjQ

IP address (v4)

*This model accepts additional fields of type array.*


# Class Name

`Ipv4`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `dnsPtr` | `?string` | Optional | Reverse DNS PTR entry for the IPv4 address of this Load Balancer | getDnsPtr(): ?string | setDnsPtr(?string dnsPtr): void |
| `ip` | `?string` | Optional | IP address (v4) of this Load Balancer | getIp(): ?string | setIp(?string ip): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\Ipv4Builder;
use HetznerCloudApiLib\ApiHelper;

$ipv4 = Ipv4Builder::init()
    ->dnsPtr('lb1.example.com')
    ->ip('1.2.3.4')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



