# Price

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRlByaWNl


# Class Name

`Price`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `location` | `string` | Required | Name of the Location the price is for | getLocation(): string | setLocation(string location): void |
| `priceHourly` | [`PriceHourly`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/price-hourly.md) | Required | Hourly costs for a Resource in this Location | getPriceHourly(): PriceHourly | setPriceHourly(PriceHourly priceHourly): void |
| `priceMonthly` | [`PriceMonthly`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/price-monthly.md) | Required | Monthly costs for a Resource in this Location | getPriceMonthly(): PriceMonthly | setPriceMonthly(PriceMonthly priceMonthly): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\PriceBuilder;
use HetznerCloudAPILib\Models\Builders\PriceHourlyBuilder;
use HetznerCloudAPILib\Models\Builders\PriceMonthlyBuilder;

$price = PriceBuilder::init(
    'fsn1',
    PriceHourlyBuilder::init(
        '1.1900000000000000',
        '1.0000000000'
    )->build(),
    PriceMonthlyBuilder::init(
        '1.1900000000000000',
        '1.0000000000'
    )->build()
)->build();
```



