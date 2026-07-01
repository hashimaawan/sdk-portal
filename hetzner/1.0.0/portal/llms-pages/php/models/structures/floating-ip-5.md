# Floating Ip 5

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkZsb2F0aW5nSXA1


# Class Name

`FloatingIp5`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `prices` | [`Price6[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/price-6.md) | Required | Floating IP type costs per Location | getPrices(): array | setPrices(array prices): void |
| `type` | [`string(Type48Enum)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/enumerations/type-48.md) | Required | The type of the Floating IP | getType(): string | setType(string type): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\FloatingIp5Builder;
use HetznerCloudAPILib\Models\Builders\Price6Builder;
use HetznerCloudAPILib\Models\Builders\PriceMonthly7Builder;
use HetznerCloudAPILib\Models\Type48Enum;

$floatingIp5 = FloatingIp5Builder::init(
    [
        Price6Builder::init(
            'fsn1',
            PriceMonthly7Builder::init(
                '1.1900000000000000',
                '1.0000000000'
            )->build()
        )->build()
    ],
    Type48Enum::IPV4
)->build();
```



