# Price 6

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlByaWNlNg

*This model accepts additional fields of type array.*


# Class Name

`Price6`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `location` | `string` | Required | Name of the Location the price is for | getLocation(): string | setLocation(string location): void |
| `priceMonthly` | [`PriceMonthly7`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/price-monthly-7.md) | Required | Monthly costs for a Floating IP type in this Location | getPriceMonthly(): PriceMonthly7 | setPriceMonthly(PriceMonthly7 priceMonthly): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\Price6Builder;
use HetznerCloudApiLib\Models\Builders\PriceMonthly7Builder;
use HetznerCloudApiLib\ApiHelper;

$price6 = Price6Builder::init(
    'fsn1',
    PriceMonthly7Builder::init(
        '1.1900000000000000',
        '1.0000000000'
    )
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build()
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



