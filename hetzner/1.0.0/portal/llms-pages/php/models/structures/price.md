# Price

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlByaWNl

*This model accepts additional fields of type array.*


# Class Name

`Price`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `location` | `string` | Required | Name of the Location the price is for | getLocation(): string | setLocation(string location): void |
| `priceHourly` | [`PriceHourly`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/price-hourly.md) | Required | Hourly costs for a Resource in this Location | getPriceHourly(): PriceHourly | setPriceHourly(PriceHourly priceHourly): void |
| `priceMonthly` | [`PriceMonthly`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/price-monthly.md) | Required | Monthly costs for a Resource in this Location | getPriceMonthly(): PriceMonthly | setPriceMonthly(PriceMonthly priceMonthly): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\PriceBuilder;
use HetznerCloudApiLib\Models\Builders\PriceHourlyBuilder;
use HetznerCloudApiLib\ApiHelper;
use HetznerCloudApiLib\Models\Builders\PriceMonthlyBuilder;

$price = PriceBuilder::init(
    'fsn1',
    PriceHourlyBuilder::init(
        '1.1900000000000000',
        '1.0000000000'
    )
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build(),
    PriceMonthlyBuilder::init(
        '1.1900000000000000',
        '1.0000000000'
    )
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build()
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



