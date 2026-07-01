# Server Types 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlNlcnZlclR5cGVzMg


# Class Name

`ServerTypes2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `id` | `float` | Required | ID of the Server type the price is for | getId(): float | setId(float id): void |
| `name` | `string` | Required | Name of the Server type the price is for | getName(): string | setName(string name): void |
| `prices` | [`Price9[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/price-9.md) | Required | Server type costs per Location | getPrices(): array | setPrices(array prices): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\ServerTypes2Builder;
use HetznerCloudAPILib\Models\Builders\Price9Builder;
use HetznerCloudAPILib\Models\Builders\PriceHourly8Builder;
use HetznerCloudAPILib\Models\Builders\PriceMonthly10Builder;

$serverTypes2 = ServerTypes2Builder::init(
    4,
    'cx11',
    [
        Price9Builder::init(
            'fsn1',
            PriceHourly8Builder::init(
                '1.1900000000000000',
                '1.0000000000'
            )->build(),
            PriceMonthly10Builder::init(
                '1.1900000000000000',
                '1.0000000000'
            )->build()
        )->build()
    ]
)->build();
```



