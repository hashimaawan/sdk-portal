# Networks Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRk5ldHdvcmtzJTI1MjBSZXNwb25zZQ


# Class Name

`NetworksResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `meta` | [`?Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/meta.md) | Optional | - | getMeta(): ?Meta | setMeta(?Meta meta): void |
| `networks` | [`Network[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/network.md) | Required | - | getNetworks(): array | setNetworks(array networks): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\NetworksResponseBuilder;
use HetznerCloudAPILib\Models\Builders\NetworkBuilder;
use HetznerCloudAPILib\ApiHelper;
use HetznerCloudAPILib\Models\Builders\Protection11Builder;
use HetznerCloudAPILib\Models\Builders\RouteBuilder;
use HetznerCloudAPILib\Models\Builders\SubnetBuilder;
use HetznerCloudAPILib\Models\Type42Enum;
use HetznerCloudAPILib\Models\Builders\MetaBuilder;
use HetznerCloudAPILib\Models\Builders\PaginationBuilder;

$networksResponse = NetworksResponseBuilder::init(
    [
        NetworkBuilder::init(
            '2016-01-30T23:50:00+00:00',
            4711,
            '10.0.0.0/16',
            ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'),
            'mynet',
            Protection11Builder::init(
                false
            )->build(),
            [
                RouteBuilder::init(
                    '10.100.1.0/24',
                    '10.0.1.1'
                )->build()
            ],
            [
                42
            ],
            [
                SubnetBuilder::init(
                    '10.0.0.1',
                    'eu-central',
                    Type42Enum::CLOUD
                )
                    ->ipRange('10.0.1.0/24')
                    ->build()
            ]
        )
            ->loadBalancers(
                [
                    42
                ]
            )
            ->build()
    ]
)
    ->meta(
        MetaBuilder::init(
            PaginationBuilder::init(
                17.58,
                13.34
            )
                ->lastPage(77.7)
                ->nextPage(209.18)
                ->previousPage(50.02)
                ->totalEntries(206.64)
                ->build()
        )->build()
    )->build();
```



