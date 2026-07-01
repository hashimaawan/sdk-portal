# Price 8

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlByaWNlOA

*This model accepts additional fields of type array.*


# Class Name

`Price8`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `location` | `string` | Required | Name of the Location the price is for | getLocation(): string | setLocation(string location): void |
| `priceHourly` | [`PriceHourly7`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/price-hourly-7.md) | Required | Hourly costs for a Primary IP type in this Location | getPriceHourly(): PriceHourly7 | setPriceHourly(PriceHourly7 priceHourly): void |
| `priceMonthly` | [`PriceMonthly9`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/price-monthly-9.md) | Required | Monthly costs for a Primary IP type in this Location | getPriceMonthly(): PriceMonthly9 | setPriceMonthly(PriceMonthly9 priceMonthly): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\Price8Builder;
use HetznerCloudApiLib\Models\Builders\PriceHourly7Builder;
use HetznerCloudApiLib\ApiHelper;
use HetznerCloudApiLib\Models\Builders\PriceMonthly9Builder;

$price8 = Price8Builder::init(
    'fsn1',
    PriceHourly7Builder::init(
        '1.1900000000000000',
        '1.0000000000'
    )
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build(),
    PriceMonthly9Builder::init(
        '1.1900000000000000',
        '1.0000000000'
    )
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build()
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



