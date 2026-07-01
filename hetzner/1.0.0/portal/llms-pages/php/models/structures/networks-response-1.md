# Networks Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRk5ldHdvcmtzJTI1MjBSZXNwb25zZTE


# Class Name

`NetworksResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `network` | [`?Network`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/network.md) | Optional | - | getNetwork(): ?Network | setNetwork(?Network network): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\NetworksResponse1Builder;
use HetznerCloudAPILib\Models\Builders\NetworkBuilder;
use HetznerCloudAPILib\ApiHelper;
use HetznerCloudAPILib\Models\Builders\Protection11Builder;
use HetznerCloudAPILib\Models\Builders\RouteBuilder;
use HetznerCloudAPILib\Models\Builders\SubnetBuilder;
use HetznerCloudAPILib\Models\Type42Enum;

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
            )->build(),
            [
                RouteBuilder::init(
                    'destination8',
                    'gateway6'
                )->build(),
                RouteBuilder::init(
                    'destination8',
                    'gateway6'
                )->build(),
                RouteBuilder::init(
                    'destination8',
                    'gateway6'
                )->build()
            ],
            [
                93
            ],
            [
                SubnetBuilder::init(
                    'gateway4',
                    'network_zone2',
                    Type42Enum::CLOUD
                )
                    ->ipRange('ip_range6')
                    ->build()
            ]
        )
            ->loadBalancers(
                [
                    208
                ]
            )
            ->build()
    )
    ->build();
```



