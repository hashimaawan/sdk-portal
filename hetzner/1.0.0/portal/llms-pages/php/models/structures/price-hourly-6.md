# Price Hourly 6

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlByaWNlSG91cmx5Ng

Hourly costs for a Load Balancer type in this network zone


# Class Name

`PriceHourly6`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `gross` | `string` | Required | Price with VAT added | getGross(): string | setGross(string gross): void |
| `net` | `string` | Required | Price without VAT | getNet(): string | setNet(string net): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\PriceHourly6Builder;

$priceHourly6 = PriceHourly6Builder::init(
    '1.1900000000000000',
    '1.0000000000'
)->build();
```



