# Load Balancer Types Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VyJTI1MjBUeXBlcyUyNTIwUmVzcG9uc2Ux

*This model accepts additional fields of type array.*


# Class Name

`LoadBalancerTypesResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `loadBalancerType` | [`?LoadBalancerType`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/load-balancer-type.md) | Optional | - | getLoadBalancerType(): ?LoadBalancerType | setLoadBalancerType(?LoadBalancerType loadBalancerType): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\LoadBalancerTypesResponse1Builder;
use HetznerCloudApiLib\Models\Builders\LoadBalancerTypeBuilder;
use HetznerCloudApiLib\Models\Builders\PriceBuilder;
use HetznerCloudApiLib\Models\Builders\PriceHourlyBuilder;
use HetznerCloudApiLib\ApiHelper;
use HetznerCloudApiLib\Models\Builders\PriceMonthlyBuilder;

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
                    )
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build(),
                    PriceMonthlyBuilder::init(
                        'gross2',
                        'net0'
                    )
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build(),
                PriceBuilder::init(
                    'location8',
                    PriceHourlyBuilder::init(
                        'gross4',
                        'net2'
                    )
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build(),
                    PriceMonthlyBuilder::init(
                        'gross2',
                        'net0'
                    )
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build(),
                PriceBuilder::init(
                    'location8',
                    PriceHourlyBuilder::init(
                        'gross4',
                        'net2'
                    )
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build(),
                    PriceMonthlyBuilder::init(
                        'gross2',
                        'net0'
                    )
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            ]
        )
            ->deprecated('deprecated2')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



