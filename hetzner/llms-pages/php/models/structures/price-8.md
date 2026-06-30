# Price 8

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRlByaWNlOA


# Class Name

`Price8`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `location` | `string` | Required | Name of the Location the price is for | getLocation(): string | setLocation(string location): void |
| `priceHourly` | [`PriceHourly7`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/price-hourly-7.md) | Required | Hourly costs for a Primary IP type in this Location | getPriceHourly(): PriceHourly7 | setPriceHourly(PriceHourly7 priceHourly): void |
| `priceMonthly` | [`PriceMonthly9`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/price-monthly-9.md) | Required | Monthly costs for a Primary IP type in this Location | getPriceMonthly(): PriceMonthly9 | setPriceMonthly(PriceMonthly9 priceMonthly): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\Price8Builder;
use HetznerCloudAPILib\Models\Builders\PriceHourly7Builder;
use HetznerCloudAPILib\Models\Builders\PriceMonthly9Builder;

$price8 = Price8Builder::init(
    'fsn1',
    PriceHourly7Builder::init(
        '1.1900000000000000',
        '1.0000000000'
    )->build(),
    PriceMonthly9Builder::init(
        '1.1900000000000000',
        '1.0000000000'
    )->build()
)->build();
```



