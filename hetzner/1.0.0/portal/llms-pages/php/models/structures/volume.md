# Volume

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlZvbHVtZQ

The cost of Volume per GB/month


# Class Name

`Volume`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `pricePerGbMonth` | [`PricePerGbMonth`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/price-per-gb-month.md) | Required | - | getPricePerGbMonth(): PricePerGbMonth | setPricePerGbMonth(PricePerGbMonth pricePerGbMonth): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\VolumeBuilder;
use HetznerCloudAPILib\Models\Builders\PricePerGbMonthBuilder;

$volume = VolumeBuilder::init(
    PricePerGbMonthBuilder::init(
        '1.1900000000000000',
        '1.0000000000'
    )->build()
)->build();
```



