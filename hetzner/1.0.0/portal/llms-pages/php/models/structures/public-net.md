# Public Net

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlB1YmxpY05ldA

Public network information

*This model accepts additional fields of type array.*


# Class Name

`PublicNet`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `enabled` | `bool` | Required | Public Interface enabled or not | getEnabled(): bool | setEnabled(bool enabled): void |
| `ipv4` | [`Ipv4`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/ipv-4.md) | Required | IP address (v4) | getIpv4(): Ipv4 | setIpv4(Ipv4 ipv4): void |
| `ipv6` | [`Ipv6`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/ipv-6.md) | Required | IP address (v6) | getIpv6(): Ipv6 | setIpv6(Ipv6 ipv6): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\PublicNetBuilder;
use HetznerCloudApiLib\Models\Builders\Ipv4Builder;
use HetznerCloudApiLib\ApiHelper;
use HetznerCloudApiLib\Models\Builders\Ipv6Builder;

$publicNet = PublicNetBuilder::init(
    false,
    Ipv4Builder::init()
        ->dnsPtr('lb1.example.com')
        ->ip('1.2.3.4')
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build(),
    Ipv6Builder::init()
        ->dnsPtr('lb1.example.com')
        ->ip('2001:db8::1')
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build()
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



