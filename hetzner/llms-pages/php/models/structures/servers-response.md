# Servers Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMFJlc3BvbnNl


# Class Name

`ServersResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `meta` | [`?Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/meta.md) | Optional | - | getMeta(): ?Meta | setMeta(?Meta meta): void |
| `servers` | [`Server18[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/server-18.md) | Required | - | getServers(): array | setServers(array servers): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\ServersResponseBuilder;
use HetznerCloudAPILib\Models\Builders\Server18Builder;
use HetznerCloudAPILib\Models\Builders\Datacenter6Builder;
use HetznerCloudAPILib\Models\Builders\LocationBuilder;
use HetznerCloudAPILib\Models\Builders\ServerTypesBuilder;
use HetznerCloudAPILib\Models\Builders\PrivateNet4Builder;
use HetznerCloudAPILib\Models\Builders\Protection20Builder;
use HetznerCloudAPILib\Models\Builders\PublicNet4Builder;
use HetznerCloudAPILib\Models\Builders\ServerPublicNetFirewallBuilder;
use HetznerCloudAPILib\Models\Status72Enum;
use HetznerCloudAPILib\Models\Builders\Ipv44Builder;
use HetznerCloudAPILib\Models\Builders\Ipv64Builder;
use HetznerCloudAPILib\Models\Builders\DnsPtr8Builder;
use HetznerCloudAPILib\Models\Builders\ServerType1Builder;
use HetznerCloudAPILib\Models\CpuTypeEnum;
use HetznerCloudAPILib\Models\Builders\Price9Builder;
use HetznerCloudAPILib\Models\Builders\PriceHourly8Builder;
use HetznerCloudAPILib\Models\Builders\PriceMonthly10Builder;
use HetznerCloudAPILib\Models\StorageTypeEnum;
use HetznerCloudAPILib\Models\Status73Enum;
use HetznerCloudAPILib\Models\Builders\ImageBuilder;
use HetznerCloudAPILib\Models\OsFlavorEnum;
use HetznerCloudAPILib\Models\Builders\ProtectionBuilder;
use HetznerCloudAPILib\Models\Status24Enum;
use HetznerCloudAPILib\Models\Type22Enum;
use HetznerCloudAPILib\Models\Builders\CreatedFromBuilder;
use HetznerCloudAPILib\Models\Builders\Iso2Builder;
use HetznerCloudAPILib\Models\Type26Enum;
use HetznerCloudAPILib\Models\Builders\PlacementGroupNullableBuilder;
use HetznerCloudAPILib\Models\Builders\MetaBuilder;
use HetznerCloudAPILib\Models\Builders\PaginationBuilder;

$serversResponse = ServersResponseBuilder::init(
    [
        Server18Builder::init(
            '2016-01-30T23:55:00+00:00',
            Datacenter6Builder::init(
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
            42,
            [
                'key0' => 'labels0'
            ],
            false,
            'my-resource',
            50,
            [
                PrivateNet4Builder::init()
                    ->aliasIps(
                        [
                            'alias_ips4'
                        ]
                    )
                    ->ip('10.0.0.2')
                    ->macAddress('86:00:ff:2a:7d:e1')
                    ->network(4711)
                    ->build()
            ],
            Protection20Builder::init(
                false,
                false
            )->build(),
            PublicNet4Builder::init(
                [
                    478
                ]
            )
                ->firewalls(
                    [
                        ServerPublicNetFirewallBuilder::init()
                            ->id(250)
                            ->status(Status72Enum::APPLIED)
                            ->build(),
                        ServerPublicNetFirewallBuilder::init()
                            ->id(250)
                            ->status(Status72Enum::APPLIED)
                            ->build()
                    ]
                )
                ->ipv4(
                    Ipv44Builder::init(
                        false,
                        'server01.example.com',
                        '1.2.3.4'
                    )
                        ->id(42)
                        ->build()
                )
                ->ipv6(
                    Ipv64Builder::init(
                        false,
                        '2001:db8::/64'
                    )
                        ->dnsPtr(
                            [
                                DnsPtr8Builder::init(
                                    'server.example.com',
                                    '2001:db8::1'
                                )->build()
                            ]
                        )
                        ->id(42)
                        ->build()
                )
                ->build(),
            false,
            ServerType1Builder::init(
                1,
                CpuTypeEnum::SHARED,
                false,
                'CX11',
                25,
                1,
                1,
                'cx11',
                [
                    Price9Builder::init(
                        'fsn1',
                        PriceHourly8Builder::init(
                            '1.1900000000000000',
                            '1.0000000000'
                        )->build(),
                        PriceMonthly10Builder::init(
                            '1.1900000000000000',
                            '1.0000000000'
                        )->build()
                    )->build()
                ],
                StorageTypeEnum::LOCAL
            )->build(),
            Status73Enum::STARTING
        )
            ->backupWindow('22-02')
            ->image(
                ImageBuilder::init(
                    '2016-01-30T23:55:00+00:00',
                    'Ubuntu 20.04 Standard 64 bit',
                    10,
                    42,
                    [
                        'key0' => 'labels4'
                    ],
                    OsFlavorEnum::UBUNTU,
                    ProtectionBuilder::init(
                        false
                    )->build(),
                    Status24Enum::UNAVAILABLE,
                    Type22Enum::SNAPSHOT
                )
                    ->boundTo(null)
                    ->createdFrom(
                        CreatedFromBuilder::init(
                            1,
                            'Server'
                        )->build()
                    )
                    ->deleted(null)
                    ->deprecated('2018-02-28T00:00:00+00:00')
                    ->imageSize(2.3)
                    ->name('ubuntu-20.04')
                    ->osVersion('20.04')
                    ->rapidDeploy(false)
                    ->build()
            )
            ->includedTraffic(654321)
            ->ingoingTraffic(123456)
            ->iso(
                Iso2Builder::init(
                    'FreeBSD 11.0 x64',
                    42,
                    Type26Enum::PUBLIC_
                )
                    ->deprecated('2018-02-28T00:00:00+00:00')
                    ->name('FreeBSD-11.0-RELEASE-amd64-dvd1')
                    ->build()
            )
            ->loadBalancers(
                [
                    128,
                    129,
                    130
                ]
            )
            ->outgoingTraffic(123456)
            ->placementGroup(
                PlacementGroupNullableBuilder::init(
                    'created8',
                    236,
                    [
                        'key0' => 'labels4'
                    ],
                    'name8',
                    [
                        251,
                        252,
                        253
                    ]
                )->build()
            )
            ->volumes(
                [
                    177
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



