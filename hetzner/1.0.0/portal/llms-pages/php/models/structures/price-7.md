# Price 7

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlByaWNlNw

*This model accepts additional fields of type array.*


# Class Name

`Price7`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `location` | `string` | Required | Name of the Location the price is for | getLocation(): string | setLocation(string location): void |
| `priceHourly` | [`PriceHourly6`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/price-hourly-6.md) | Required | Hourly costs for a Load Balancer type in this network zone | getPriceHourly(): PriceHourly6 | setPriceHourly(PriceHourly6 priceHourly): void |
| `priceMonthly` | [`PriceMonthly8`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/price-monthly-8.md) | Required | Monthly costs for a Load Balancer type in this network zone | getPriceMonthly(): PriceMonthly8 | setPriceMonthly(PriceMonthly8 priceMonthly): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\Price7Builder;
use HetznerCloudApiLib\Models\Builders\PriceHourly6Builder;
use HetznerCloudApiLib\ApiHelper;
use HetznerCloudApiLib\Models\Builders\PriceMonthly8Builder;

$price7 = Price7Builder::init(
    'fsn1',
    PriceHourly6Builder::init(
        '1.1900000000000000',
        '1.0000000000'
    )
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build(),
    PriceMonthly8Builder::init(
        '1.1900000000000000',
        '1.0000000000'
    )
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build()
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



