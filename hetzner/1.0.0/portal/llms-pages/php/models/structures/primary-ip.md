# Primary Ip

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlByaW1hcnlJcA

*This model accepts additional fields of type array.*


# Class Name

`PrimaryIp`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `prices` | [`Price8[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/price-8.md) | Required | Primary IP type costs per Location | getPrices(): array | setPrices(array prices): void |
| `type` | [`string(Type49)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/enumerations/type-49.md) | Required | The type of the Primary IP | getType(): string | setType(string type): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\PrimaryIpBuilder;
use HetznerCloudApiLib\Models\Builders\Price8Builder;
use HetznerCloudApiLib\Models\Builders\PriceHourly7Builder;
use HetznerCloudApiLib\ApiHelper;
use HetznerCloudApiLib\Models\Builders\PriceMonthly9Builder;
use HetznerCloudApiLib\Models\Type49;

$primaryIp = PrimaryIpBuilder::init(
    [
        Price8Builder::init(
            'fsn1',
            PriceHourly7Builder::init(
                '1.1900000000000000',
                '1.0000000000'
            )
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            PriceMonthly9Builder::init(
                '1.1900000000000000',
                '1.0000000000'
            )
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    ],
    Type49::IPV4
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



