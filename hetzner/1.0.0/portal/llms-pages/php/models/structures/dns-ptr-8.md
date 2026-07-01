# Dns Ptr 8

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkRuc1B0cjg

*This model accepts additional fields of type array.*


# Class Name

`DnsPtr8`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `dnsPtr` | `string` | Required | DNS pointer for the specific IP address | getDnsPtr(): string | setDnsPtr(string dnsPtr): void |
| `ip` | `string` | Required | Single IPv6 address of this Server for which the reverse DNS entry has been set up | getIp(): string | setIp(string ip): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\DnsPtr8Builder;
use HetznerCloudApiLib\ApiHelper;

$dnsPtr8 = DnsPtr8Builder::init(
    'server.example.com',
    '2001:db8::1'
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



