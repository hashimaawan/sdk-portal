# Load Balancer Types Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VyJTI1MjBUeXBlcyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type array.*


# Class Name

`LoadBalancerTypesResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `loadBalancerTypes` | [`LoadBalancerType[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/load-balancer-type.md) | Required | - | getLoadBalancerTypes(): array | setLoadBalancerTypes(array loadBalancerTypes): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\LoadBalancerTypesResponseBuilder;
use HetznerCloudApiLib\Models\Builders\LoadBalancerTypeBuilder;
use HetznerCloudApiLib\Models\Builders\PriceBuilder;
use HetznerCloudApiLib\Models\Builders\PriceHourlyBuilder;
use HetznerCloudApiLib\ApiHelper;
use HetznerCloudApiLib\Models\Builders\PriceMonthlyBuilder;

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
                    )
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build(),
                    PriceMonthlyBuilder::init(
                        '1.1900000000000000',
                        '1.0000000000'
                    )
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            ]
        )
            ->deprecated('2016-01-30T23:50:00+00:00')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    ]
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



