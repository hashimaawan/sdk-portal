# Primary Ip

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRlByaW1hcnlJcA


# Class Name

`PrimaryIp`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `prices` | [`Price8[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/price-8.md) | Required | Primary IP type costs per Location | getPrices(): array | setPrices(array prices): void |
| `type` | [`string(Type49Enum)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/enumerations/type-49.md) | Required | The type of the Primary IP | getType(): string | setType(string type): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\PrimaryIpBuilder;
use HetznerCloudAPILib\Models\Builders\Price8Builder;
use HetznerCloudAPILib\Models\Builders\PriceHourly7Builder;
use HetznerCloudAPILib\Models\Builders\PriceMonthly9Builder;
use HetznerCloudAPILib\Models\Type49Enum;

$primaryIp = PrimaryIpBuilder::init(
    [
        Price8Builder::init(
            'fsn1',
            PriceHourly7Builder::init(
                '1.1900000000000000',
                '1.0000000000'
            )->build(),
            PriceMonthly9Builder::init(
                '1.1900000000000000',
                '1.0000000000'
            )->build()
        )->build()
    ],
    Type49Enum::IPV4
)->build();
```



