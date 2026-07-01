# Floating Ip 4

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkZsb2F0aW5nSXA0

The cost of one Floating IP per month

*This model accepts additional fields of type array.*


# Class Name

`FloatingIp4`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `priceMonthly` | [`PriceMonthly6`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/price-monthly-6.md) | Required | - | getPriceMonthly(): PriceMonthly6 | setPriceMonthly(PriceMonthly6 priceMonthly): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\FloatingIp4Builder;
use HetznerCloudApiLib\Models\Builders\PriceMonthly6Builder;
use HetznerCloudApiLib\ApiHelper;

$floatingIp4 = FloatingIp4Builder::init(
    PriceMonthly6Builder::init(
        '1.1900000000000000',
        '1.0000000000'
    )
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build()
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



