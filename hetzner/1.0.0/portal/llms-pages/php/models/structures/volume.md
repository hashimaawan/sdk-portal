# Volume

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlZvbHVtZQ

The cost of Volume per GB/month

*This model accepts additional fields of type array.*


# Class Name

`Volume`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `pricePerGbMonth` | [`PricePerGbMonth`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/price-per-gb-month.md) | Required | - | getPricePerGbMonth(): PricePerGbMonth | setPricePerGbMonth(PricePerGbMonth pricePerGbMonth): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\VolumeBuilder;
use HetznerCloudApiLib\Models\Builders\PricePerGbMonthBuilder;
use HetznerCloudApiLib\ApiHelper;

$volume = VolumeBuilder::init(
    PricePerGbMonthBuilder::init(
        '1.1900000000000000',
        '1.0000000000'
    )
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build()
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



