# Floating Ip 4

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRkZsb2F0aW5nSXA0

The cost of one Floating IP per month


# Class Name

`FloatingIp4`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `priceMonthly` | [`PriceMonthly6`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/price-monthly-6.md) | Required | - | getPriceMonthly(): PriceMonthly6 | setPriceMonthly(PriceMonthly6 priceMonthly): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\FloatingIp4Builder;
use HetznerCloudAPILib\Models\Builders\PriceMonthly6Builder;

$floatingIp4 = FloatingIp4Builder::init(
    PriceMonthly6Builder::init(
        '1.1900000000000000',
        '1.0000000000'
    )->build()
)->build();
```



