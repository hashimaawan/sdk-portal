# Load Balancer Types Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VyJTI1MjBUeXBlcyUyNTIwUmVzcG9uc2U


# Class Name

`LoadBalancerTypesResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `loadBalancerTypes` | [`LoadBalancerType[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/load-balancer-type.md) | Required | - | getLoadBalancerTypes(): array | setLoadBalancerTypes(array loadBalancerTypes): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\LoadBalancerTypesResponseBuilder;
use HetznerCloudAPILib\Models\Builders\LoadBalancerTypeBuilder;
use HetznerCloudAPILib\Models\Builders\PriceBuilder;
use HetznerCloudAPILib\Models\Builders\PriceHourlyBuilder;
use HetznerCloudAPILib\Models\Builders\PriceMonthlyBuilder;

$loadBalancerTypesResponse = LoadBalancerTypesResponseBuilder::init(
    [
        LoadBalancerTypeBuilder::init(
            'LB11',
            1,
            10,
            20000,
            5,
            25,
            'lb11',
            [
                PriceBuilder::init(
                    'fsn1',
                    PriceHourlyBuilder::init(
                        '1.1900000000000000',
                        '1.0000000000'
                    )->build(),
                    PriceMonthlyBuilder::init(
                        '1.1900000000000000',
                        '1.0000000000'
                    )->build()
                )->build()
            ]
        )
            ->deprecated('2016-01-30T23:50:00+00:00')
            ->build()
    ]
)->build();
```



