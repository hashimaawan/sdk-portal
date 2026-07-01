# Load Balancer Type 6

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlclR5cGU2


# Class Name

`LoadBalancerType6`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `id` | `float` | Required | ID of the Load Balancer type the price is for | getId(): float | setId(float id): void |
| `name` | `string` | Required | Name of the Load Balancer type the price is for | getName(): string | setName(string name): void |
| `prices` | [`Price7[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/price-7.md) | Required | Load Balancer type costs per Location | getPrices(): array | setPrices(array prices): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\LoadBalancerType6Builder;
use HetznerCloudAPILib\Models\Builders\Price7Builder;
use HetznerCloudAPILib\Models\Builders\PriceHourly6Builder;
use HetznerCloudAPILib\Models\Builders\PriceMonthly8Builder;

$loadBalancerType6 = LoadBalancerType6Builder::init(
    1,
    'lb11',
    [
        Price7Builder::init(
            'fsn1',
            PriceHourly6Builder::init(
                '1.1900000000000000',
                '1.0000000000'
            )->build(),
            PriceMonthly8Builder::init(
                '1.1900000000000000',
                '1.0000000000'
            )->build()
        )->build()
    ]
)->build();
```



