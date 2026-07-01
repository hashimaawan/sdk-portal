# Price Monthly 9

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlByaWNlTW9udGhseTk

Monthly costs for a Primary IP type in this Location


# Class Name

`PriceMonthly9`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `gross` | `string` | Required | Price with VAT added | getGross(): string | setGross(string gross): void |
| `net` | `string` | Required | Price without VAT | getNet(): string | setNet(string net): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\PriceMonthly9Builder;

$priceMonthly9 = PriceMonthly9Builder::init(
    '1.1900000000000000',
    '1.0000000000'
)->build();
```



