# Price Hourly 8

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlByaWNlSG91cmx5OA

Hourly costs for a Server type in this Location


# Class Name

`PriceHourly8`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `gross` | `string` | Required | Price with VAT added | getGross(): string | setGross(string gross): void |
| `net` | `string` | Required | Price without VAT | getNet(): string | setNet(string net): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\PriceHourly8Builder;

$priceHourly8 = PriceHourly8Builder::init(
    '1.1900000000000000',
    '1.0000000000'
)->build();
```



