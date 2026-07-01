# Create Server Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkNyZWF0ZVNlcnZlclJlc3BvbnNl

*This model accepts additional fields of type array.*


# Class Name

`CreateServerResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `action` | [`Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/action.md) | Required | - | getAction(): Action | setAction(Action action): void |
| `nextActions` | [`Action[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/action.md) | Required | - | getNextActions(): array | setNextActions(array nextActions): void |
| `rootPassword` | `?string` | Required | Root password when no SSH keys have been specified | getRootPassword(): ?string | setRootPassword(?string rootPassword): void |
| `server` | [`Server18`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/server-18.md) | Required | - | getServer(): Server18 | setServer(Server18 server): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\CreateServerResponseBuilder;
use HetznerCloudApiLib\Models\Builders\ActionBuilder;
use HetznerCloudApiLib\Models\Builders\Resource2Builder;
use HetznerCloudApiLib\ApiHelper;
use HetznerCloudApiLib\Models\Status;
use HetznerCloudApiLib\Models\Builders\ErrorBuilder;
use HetznerCloudApiLib\Models\Builders\Server18Builder;
use HetznerCloudApiLib\Models\Builders\Datacenter6Builder;
use HetznerCloudApiLib\Models\Builders\LocationBuilder;
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

$createServerResponse = CreateServerResponseBuilder::init(
    ActionBuilder::init(
        'start_server',
        42,
        100,
        [
            Resource2Builder::init(
                42,
                'server'
            )
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ],
        '2016-01-30T23:55:00+00:00',
        Status::RUNNING
    )
        ->error(
            ErrorBuilder::init(
                'action_failed',
                'Action failed'
            )
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        )
        ->finished('2016-01-30T23:55:00+00:00')
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build(),
    [
        ActionBuilder::init(
            'start_server',
            42,
            100,
            [
                Resource2Builder::init(
                    42,
                    'server'
                )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            ],
            '2016-01-30T23:55:00+00:00',
            Status::SUCCESS
        )
            ->error(
                ErrorBuilder::init(
                    'action_failed',
                    'Action failed'
                )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            )
            ->finished('2016-01-30T23:55:00+00:00')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    ],
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
            )
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
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
            )
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build(),
        42,
        [
            'key0' => 'labels0',
            'key1' => 'labels9'
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
                478
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
                    'server01.example.com',
                    '1.2.3.4'
                )
                    ->id(42)
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
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
                            )
                                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                ->build()
                        ]
                    )
                    ->id(42)
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build(),
        false,
        ServerType1Builder::init(
            1,
            CpuType::SHARED,
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
                    )
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build(),
                    PriceMonthly10Builder::init(
                        '1.1900000000000000',
                        '1.0000000000'
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
                OsFlavor::UBUNTU,
                ProtectionBuilder::init(
                    false
                )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build(),
                Status24::UNAVAILABLE,
                Type22::SNAPSHOT
            )
                ->boundTo(null)
                ->createdFrom(
                    CreatedFromBuilder::init(
                        1,
                        'Server'
                    )
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                )
                ->deleted(null)
                ->deprecated('2018-02-28T00:00:00+00:00')
                ->imageSize(2.3)
                ->name('ubuntu-20.04')
                ->osVersion('20.04')
                ->rapidDeploy(false)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        )
        ->includedTraffic(654321)
        ->ingoingTraffic(123456)
        ->iso(
            Iso2Builder::init(
                'FreeBSD 11.0 x64',
                42,
                Type26::PUBLIC_
            )
                ->deprecated('2018-02-28T00:00:00+00:00')
                ->name('FreeBSD-11.0-RELEASE-amd64-dvd1')
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
    ->rootPassword('YItygq1v3GYjjMomLaKc')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



