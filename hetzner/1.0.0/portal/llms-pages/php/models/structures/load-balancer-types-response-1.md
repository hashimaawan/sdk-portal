# Load Balancer Types Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VyJTI1MjBUeXBlcyUyNTIwUmVzcG9uc2Ux


# Class Name

`LoadBalancerTypesResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `loadBalancerType` | [`?LoadBalancerType`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/load-balancer-type.md) | Optional | - | getLoadBalancerType(): ?LoadBalancerType | setLoadBalancerType(?LoadBalancerType loadBalancerType): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\LoadBalancerTypesResponse1Builder;
use HetznerCloudAPILib\Models\Builders\LoadBalancerTypeBuilder;
use HetznerCloudAPILib\Models\Builders\PriceBuilder;
use HetznerCloudAPILib\Models\Builders\PriceHourlyBuilder;
use HetznerCloudAPILib\Models\Builders\PriceMonthlyBuilder;

$loadBalancerTypesResponse1 = LoadBalancerTypesResponse1Builder::init()
    ->loadBalancerType(
        LoadBalancerTypeBuilder::init(
            'description4',
            205.06,
            211.64,
            136.32,
            199.18,
            152.52,
            'name6',
            [
                PriceBuilder::init(
                    'location8',
                    PriceHourlyBuilder::init(
                        'gross4',
                        'net2'
                    )->build(),
                    PriceMonthlyBuilder::init(
                        'gross2',
                        'net0'
                    )->build()
                )->build(),
                PriceBuilder::init(
                    'location8',
                    PriceHourlyBuilder::init(
                        'gross4',
                        'net2'
                    )->build(),
                    PriceMonthlyBuilder::init(
                        'gross2',
                        'net0'
                    )->build()
                )->build(),
                PriceBuilder::init(
                    'location8',
                    PriceHourlyBuilder::init(
                        'gross4',
                        'net2'
                    )->build(),
                    PriceMonthlyBuilder::init(
                        'gross2',
                        'net0'
                    )->build()
                )->build()
            ]
        )
            ->deprecated('deprecated2')
            ->build()
    )
    ->build();
```



