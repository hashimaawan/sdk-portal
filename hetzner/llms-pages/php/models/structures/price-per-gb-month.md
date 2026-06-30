# Price per Gb Month

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRlByaWNlUGVyR2JNb250aA


# Class Name

`PricePerGbMonth`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `gross` | `string` | Required | Price with VAT added | getGross(): string | setGross(string gross): void |
| `net` | `string` | Required | Price without VAT | getNet(): string | setNet(string net): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\PricePerGbMonthBuilder;

$pricePerGbMonth = PricePerGbMonthBuilder::init(
    '1.1900000000000000',
    '1.0000000000'
)->build();
```



