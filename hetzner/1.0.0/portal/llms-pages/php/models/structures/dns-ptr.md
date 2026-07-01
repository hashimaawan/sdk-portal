# Dns Ptr

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkRuc1B0cg

*This model accepts additional fields of type array.*


# Class Name

`DnsPtr`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `dnsPtr` | `string` | Required | DNS pointer for the specific IP address | getDnsPtr(): string | setDnsPtr(string dnsPtr): void |
| `ip` | `string` | Required | Single IPv4 or IPv6 address | getIp(): string | setIp(string ip): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\DnsPtrBuilder;
use HetznerCloudApiLib\ApiHelper;

$dnsPtr = DnsPtrBuilder::init(
    'server.example.com',
    '2001:db8::1'
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



