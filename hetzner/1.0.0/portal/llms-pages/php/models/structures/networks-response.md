# Networks Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRk5ldHdvcmtzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type array.*


# Class Name

`NetworksResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `meta` | [`?Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/meta.md) | Optional | - | getMeta(): ?Meta | setMeta(?Meta meta): void |
| `networks` | [`Network[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/network.md) | Required | - | getNetworks(): array | setNetworks(array networks): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\NetworksResponseBuilder;
use HetznerCloudApiLib\Models\Builders\NetworkBuilder;
use HetznerCloudApiLib\ApiHelper;
use HetznerCloudApiLib\Models\Builders\Protection11Builder;
use HetznerCloudApiLib\Models\Builders\RouteBuilder;
use HetznerCloudApiLib\Models\Builders\SubnetBuilder;
use HetznerCloudApiLib\Models\Type42;
use HetznerCloudApiLib\Models\Builders\MetaBuilder;
use HetznerCloudApiLib\Models\Builders\PaginationBuilder;

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
            )
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            [
                RouteBuilder::init(
                    '10.100.1.0/24',
                    '10.0.1.1'
                )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            ],
            [
                42
            ],
            [
                SubnetBuilder::init(
                    '10.0.0.1',
                    'eu-central',
                    Type42::CLOUD
                )
                    ->ipRange('10.0.1.0/24')
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            ]
        )
            ->loadBalancers(
                [
                    42
                ]
            )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
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
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



