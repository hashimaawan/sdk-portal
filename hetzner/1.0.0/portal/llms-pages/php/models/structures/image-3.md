# Image 3

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkltYWdlMw

The cost of Image per GB/month


# Class Name

`Image3`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `pricePerGbMonth` | [`PricePerGbMonth`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/price-per-gb-month.md) | Required | - | getPricePerGbMonth(): PricePerGbMonth | setPricePerGbMonth(PricePerGbMonth pricePerGbMonth): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\Image3Builder;
use HetznerCloudAPILib\Models\Builders\PricePerGbMonthBuilder;

$image3 = Image3Builder::init(
    PricePerGbMonthBuilder::init(
        '1.1900000000000000',
        '1.0000000000'
    )->build()
)->build();
```



