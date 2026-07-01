# Price 9

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlByaWNlOQ


# Class Name

`Price9`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `location` | `string` | Required | Name of the Location the price is for | getLocation(): string | setLocation(string location): void |
| `priceHourly` | [`PriceHourly8`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/price-hourly-8.md) | Required | Hourly costs for a Server type in this Location | getPriceHourly(): PriceHourly8 | setPriceHourly(PriceHourly8 priceHourly): void |
| `priceMonthly` | [`PriceMonthly10`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/price-monthly-10.md) | Required | Monthly costs for a Server type in this Location | getPriceMonthly(): PriceMonthly10 | setPriceMonthly(PriceMonthly10 priceMonthly): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\Price9Builder;
use HetznerCloudAPILib\Models\Builders\PriceHourly8Builder;
use HetznerCloudAPILib\Models\Builders\PriceMonthly10Builder;

$price9 = Price9Builder::init(
    'fsn1',
    PriceHourly8Builder::init(
        '1.1900000000000000',
        '1.0000000000'
    )->build(),
    PriceMonthly10Builder::init(
        '1.1900000000000000',
        '1.0000000000'
    )->build()
)->build();
```



