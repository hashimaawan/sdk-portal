# Servers Response 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMFJlc3BvbnNlMg

*This model accepts additional fields of type array.*


# Class Name

`ServersResponse2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `server` | [`?Server18`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/server-18.md) | Optional | - | getServer(): ?Server18 | setServer(?Server18 server): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\ServersResponse2Builder;
use HetznerCloudApiLib\Models\Builders\Server18Builder;
use HetznerCloudApiLib\Models\Builders\Datacenter6Builder;
use HetznerCloudApiLib\Models\Builders\LocationBuilder;
use HetznerCloudApiLib\ApiHelper;
use HetznerCloudApiLib\Models\Builders\ServerTypesBuilder;
use HetznerCloudApiLib\Models\Builders\PrivateNet4Builder;
use HetznerCloudApiLib\Models\Builders\Protection20Builder;
use HetznerCloudApiLib\Models\Builders\PublicNet4Builder;
use HetznerCloudApiLib\Models\Builders\ServerPublicNetFirewallBuilder;
use HetznerCloudApiLib\Models\Status72;
use HetznerCloudApiLib\Models\Builders\Ipv44Builder;
use HetznerCloudApiLib\Models\Builders\Ipv64Builder;
use HetznerCloudApiLib\Models\Builders\DnsPtr8Builder;
use HetznerCloudApiLib\Models\Builders\ServerType1Builder;
use HetznerCloudApiLib\Models\CpuType;
use HetznerCloudApiLib\Models\Builders\Price9Builder;
use HetznerCloudApiLib\Models\Builders\PriceHourly8Builder;
use HetznerCloudApiLib\Models\Builders\PriceMonthly10Builder;
use HetznerCloudApiLib\Models\StorageType;
use HetznerCloudApiLib\Models\Status73;
use HetznerCloudApiLib\Models\Builders\ImageBuilder;
use HetznerCloudApiLib\Models\OsFlavor;
use HetznerCloudApiLib\Models\Builders\ProtectionBuilder;
use HetznerCloudApiLib\Models\Status24;
use HetznerCloudApiLib\Models\Type22;
use HetznerCloudApiLib\Models\Builders\CreatedFromBuilder;
use HetznerCloudApiLib\Models\Builders\Iso2Builder;
use HetznerCloudApiLib\Models\Type26;
use HetznerCloudApiLib\Models\Builders\PlacementGroupNullableBuilder;

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
                )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build(),
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
                )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            )
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
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
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
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
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            ],
            Protection20Builder::init(
                false,
                false
            )
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
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
                            ->status(Status72::APPLIED)
                            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                            ->build(),
                        ServerPublicNetFirewallBuilder::init()
                            ->id(250)
                            ->status(Status72::APPLIED)
                            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
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
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
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
                                )
                                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                    ->build(),
                                DnsPtr8Builder::init(
                                    'dns_ptr0',
                                    'ip6'
                                )
                                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                    ->build()
                            ]
                        )
                        ->id(8)
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                )
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            false,
            ServerType1Builder::init(
                12.84,
                CpuType::SHARED,
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
                        )
                            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                            ->build(),
                        PriceMonthly10Builder::init(
                            'gross2',
                            'net0'
                        )
                            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                            ->build()
                    )
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                ],
                StorageType::LOCAL
            )
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            Status73::STARTING
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
                    OsFlavor::DEBIAN,
                    ProtectionBuilder::init(
                        false
                    )
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build(),
                    Status24::UNAVAILABLE,
                    Type22::APP
                )
                    ->boundTo(186)
                    ->createdFrom(
                        CreatedFromBuilder::init(
                            60,
                            'name6'
                        )
                            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                            ->build()
                    )
                    ->deleted('deleted4')
                    ->deprecated('deprecated8')
                    ->imageSize(141.34)
                    ->name('name6')
                    ->osVersion('os_version4')
                    ->rapidDeploy(false)
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            )
            ->includedTraffic(123.68)
            ->ingoingTraffic(151.82)
            ->iso(
                Iso2Builder::init(
                    'description2',
                    66,
                    Type26::PUBLIC_
                )
                    ->deprecated('deprecated0')
                    ->name('name8')
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
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
                )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            )
            ->volumes(
                [
                    91,
                    92
                ]
            )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



