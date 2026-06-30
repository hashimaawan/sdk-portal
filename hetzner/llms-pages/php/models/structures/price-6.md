# Price 6

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRlByaWNlNg


# Class Name

`Price6`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `location` | `string` | Required | Name of the Location the price is for | getLocation(): string | setLocation(string location): void |
| `priceMonthly` | [`PriceMonthly7`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/price-monthly-7.md) | Required | Monthly costs for a Floating IP type in this Location | getPriceMonthly(): PriceMonthly7 | setPriceMonthly(PriceMonthly7 priceMonthly): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\Price6Builder;
use HetznerCloudAPILib\Models\Builders\PriceMonthly7Builder;

$price6 = Price6Builder::init(
    'fsn1',
    PriceMonthly7Builder::init(
        '1.1900000000000000',
        '1.0000000000'
    )->build()
)->build();
```



