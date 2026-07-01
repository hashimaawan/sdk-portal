# Networks Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRk5ldHdvcmtzJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type array.*


# Class Name

`NetworksResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `network` | [`?Network`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/network.md) | Optional | - | getNetwork(): ?Network | setNetwork(?Network network): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\NetworksResponse1Builder;
use HetznerCloudApiLib\Models\Builders\NetworkBuilder;
use HetznerCloudApiLib\ApiHelper;
use HetznerCloudApiLib\Models\Builders\Protection11Builder;
use HetznerCloudApiLib\Models\Builders\RouteBuilder;
use HetznerCloudApiLib\Models\Builders\SubnetBuilder;
use HetznerCloudApiLib\Models\Type42;

$networksResponse1 = NetworksResponse1Builder::init()
    ->network(
        NetworkBuilder::init(
            'created4',
            78,
            'ip_range6',
            ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'),
            'name4',
            Protection11Builder::init(
                false
            )
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            [
                RouteBuilder::init(
                    'destination8',
                    'gateway6'
                )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build(),
                RouteBuilder::init(
                    'destination8',
                    'gateway6'
                )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build(),
                RouteBuilder::init(
                    'destination8',
                    'gateway6'
                )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            ],
            [
                93
            ],
            [
                SubnetBuilder::init(
                    'gateway4',
                    'network_zone2',
                    Type42::CLOUD
                )
                    ->ipRange('ip_range6')
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            ]
        )
            ->loadBalancers(
                [
                    208
                ]
            )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



