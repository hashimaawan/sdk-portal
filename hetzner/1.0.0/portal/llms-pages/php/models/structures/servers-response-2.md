# Servers Response 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMFJlc3BvbnNlMg


# Class Name

`ServersResponse2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `server` | [`?Server18`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/server-18.md) | Optional | - | getServer(): ?Server18 | setServer(?Server18 server): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\ServersResponse2Builder;
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

$serversResponse2 = ServersResponse2Builder::init()
    ->server(
        Server18Builder::init(
            'created4',
            Datacenter6Builder::init(
                'description0',
                200,
                LocationBuilder::init(
                    'city6',
                    'country8',
                    'description6',
                    187.14,
                    194.62,
                    59.18,
                    'name4',
                    'network_zone2'
                )->build(),
                'name0',
                ServerTypesBuilder::init(
                    [
                        23.74
                    ],
                    [
                        201.65,
                        201.66
                    ],
                    [
                        69.52,
                        69.53,
                        69.54
                    ]
                )->build()
            )->build(),
            14,
            [
                'key0' => 'labels0',
                'key1' => 'labels9'
            ],
            false,
            'name4',
            19.88,
            [
                PrivateNet4Builder::init()
                    ->aliasIps(
                        [
                            'alias_ips4'
                        ]
                    )
                    ->ip('ip6')
                    ->macAddress('mac_address0')
                    ->network(154)
                    ->build(),
                PrivateNet4Builder::init()
                    ->aliasIps(
                        [
                            'alias_ips4'
                        ]
                    )
                    ->ip('ip6')
                    ->macAddress('mac_address0')
                    ->network(154)
                    ->build()
            ],
            Protection20Builder::init(
                false,
                false
            )->build(),
            PublicNet4Builder::init(
                [
                    54,
                    55,
                    56
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
                        'dns_ptr4',
                        'ip2'
                    )
                        ->id(104)
                        ->build()
                )
                ->ipv6(
                    Ipv64Builder::init(
                        false,
                        'ip0'
                    )
                        ->dnsPtr(
                            [
                                DnsPtr8Builder::init(
                                    'dns_ptr0',
                                    'ip6'
                                )->build(),
                                DnsPtr8Builder::init(
                                    'dns_ptr0',
                                    'ip6'
                                )->build()
                            ]
                        )
                        ->id(8)
                        ->build()
                )
                ->build(),
            false,
            ServerType1Builder::init(
                12.84,
                CpuTypeEnum::SHARED,
                false,
                'description0',
                14.32,
                30,
                21.2,
                'name0',
                [
                    Price9Builder::init(
                        'location8',
                        PriceHourly8Builder::init(
                            'gross4',
                            'net2'
                        )->build(),
                        PriceMonthly10Builder::init(
                            'gross2',
                            'net0'
                        )->build()
                    )->build()
                ],
                StorageTypeEnum::LOCAL
            )->build(),
            Status73Enum::STARTING
        )
            ->backupWindow('backup_window2')
            ->image(
                ImageBuilder::init(
                    'created6',
                    'description6',
                    244.18,
                    128,
                    [
                        'key0' => 'labels4'
                    ],
                    OsFlavorEnum::DEBIAN,
                    ProtectionBuilder::init(
                        false
                    )->build(),
                    Status24Enum::UNAVAILABLE,
                    Type22Enum::APP
                )
                    ->boundTo(186)
                    ->createdFrom(
                        CreatedFromBuilder::init(
                            60,
                            'name6'
                        )->build()
                    )
                    ->deleted('deleted4')
                    ->deprecated('deprecated8')
                    ->imageSize(141.34)
                    ->name('name6')
                    ->osVersion('os_version4')
                    ->rapidDeploy(false)
                    ->build()
            )
            ->includedTraffic(123.68)
            ->ingoingTraffic(151.82)
            ->iso(
                Iso2Builder::init(
                    'description2',
                    66,
                    Type26Enum::PUBLIC_
                )
                    ->deprecated('deprecated0')
                    ->name('name8')
                    ->build()
            )
            ->loadBalancers(
                [
                    144,
                    143,
                    142
                ]
            )
            ->outgoingTraffic(129.6)
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
                    91,
                    92
                ]
            )
            ->build()
    )
    ->build();
```



