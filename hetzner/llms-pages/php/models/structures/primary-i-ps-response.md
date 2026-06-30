# Primary I Ps Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRlByaW1hcnlJUHNSZXNwb25zZQ


# Class Name

`PrimaryIPsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `meta` | [`?Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/meta.md) | Optional | - | getMeta(): ?Meta | setMeta(?Meta meta): void |
| `primaryIps` | [`PrimaryIP1[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/primary-ip-1.md) | Required | - | getPrimaryIps(): array | setPrimaryIps(array primaryIps): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\PrimaryIPsResponseBuilder;
use HetznerCloudAPILib\Models\Builders\PrimaryIP1Builder;
use HetznerCloudAPILib\Models\Builders\Datacenter2Builder;
use HetznerCloudAPILib\Models\Builders\LocationBuilder;
use HetznerCloudAPILib\Models\Builders\ServerTypesBuilder;
use HetznerCloudAPILib\Models\Builders\DnsPtrBuilder;
use HetznerCloudAPILib\Models\Builders\ProtectionBuilder;
use HetznerCloudAPILib\Models\Type50Enum;
use HetznerCloudAPILib\Models\Builders\MetaBuilder;
use HetznerCloudAPILib\Models\Builders\PaginationBuilder;

$primaryIPsResponse = PrimaryIPsResponseBuilder::init(
    [
        PrimaryIP1Builder::init(
            true,
            false,
            '2016-01-30T23:55:00+00:00',
            Datacenter2Builder::init(
                'Falkenstein DC Park 8',
                42,
                LocationBuilder::init(
                    'Falkenstein',
                    'DE',
                    'Falkenstein DC Park 1',
                    1,
                    50.47612,
                    12.370071,
                    'fsn1',
                    'eu-central'
                )->build(),
                'fsn1-dc8',
                ServerTypesBuilder::init(
                    [
                        1,
                        2,
                        3
                    ],
                    [
                        1,
                        2,
                        3
                    ],
                    [
                        1,
                        2,
                        3
                    ]
                )->build()
            )->build(),
            [
                DnsPtrBuilder::init(
                    'server.example.com',
                    '2001:db8::1'
                )->build()
            ],
            42,
            '131.232.99.1',
            [
                'key0' => 'labels2',
                'key1' => 'labels3',
                'key2' => 'labels4'
            ],
            'my-resource',
            ProtectionBuilder::init(
                false
            )->build(),
            Type50Enum::IPV4
        )
            ->assigneeId(17)
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



