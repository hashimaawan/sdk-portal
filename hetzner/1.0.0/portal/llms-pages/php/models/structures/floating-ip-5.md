# Floating Ip 5

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkZsb2F0aW5nSXA1

*This model accepts additional fields of type array.*


# Class Name

`FloatingIp5`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `prices` | [`Price6[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/price-6.md) | Required | Floating IP type costs per Location | getPrices(): array | setPrices(array prices): void |
| `type` | [`string(Type48)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/enumerations/type-48.md) | Required | The type of the Floating IP | getType(): string | setType(string type): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\FloatingIp5Builder;
use HetznerCloudApiLib\Models\Builders\Price6Builder;
use HetznerCloudApiLib\Models\Builders\PriceMonthly7Builder;
use HetznerCloudApiLib\ApiHelper;
use HetznerCloudApiLib\Models\Type48;

$floatingIp5 = FloatingIp5Builder::init(
    [
        Price6Builder::init(
            'fsn1',
            PriceMonthly7Builder::init(
                '1.1900000000000000',
                '1.0000000000'
            )
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    ],
    Type48::IPV4
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



