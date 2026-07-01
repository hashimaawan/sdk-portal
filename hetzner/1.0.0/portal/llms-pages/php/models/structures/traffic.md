# Traffic

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlRyYWZmaWM

The cost of additional traffic per TB


# Class Name

`Traffic`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `pricePerTb` | [`PricePerTb`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/price-per-tb.md) | Required | - | getPricePerTb(): PricePerTb | setPricePerTb(PricePerTb pricePerTb): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\TrafficBuilder;
use HetznerCloudAPILib\Models\Builders\PricePerTbBuilder;

$traffic = TrafficBuilder::init(
    PricePerTbBuilder::init(
        '1.1900000000000000',
        '1.0000000000'
    )->build()
)->build();
```



