# Server 18

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlNlcnZlcjE4

*This model accepts additional fields of type array.*


# Class Name

`Server18`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `backupWindow` | `?string` | Required | Time window (UTC) in which the backup will run, or null if the backups are not enabled | getBackupWindow(): ?string | setBackupWindow(?string backupWindow): void |
| `created` | `string` | Required | Point in time when the Resource was created (in ISO-8601 format) | getCreated(): string | setCreated(string created): void |
| `datacenter` | [`Datacenter6`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/datacenter-6.md) | Required | Datacenter this Resource is located at | getDatacenter(): Datacenter6 | setDatacenter(Datacenter6 datacenter): void |
| `id` | `int` | Required | ID of the Resource | getId(): int | setId(int id): void |
| `image` | [`?Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/image.md) | Required | - | getImage(): ?Image | setImage(?Image image): void |
| `includedTraffic` | `?float` | Required | Free Traffic for the current billing period in bytes | getIncludedTraffic(): ?float | setIncludedTraffic(?float includedTraffic): void |
| `ingoingTraffic` | `?float` | Required | Inbound Traffic for the current billing period in bytes | getIngoingTraffic(): ?float | setIngoingTraffic(?float ingoingTraffic): void |
| `iso` | [`?Iso2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/iso-2.md) | Required | ISO Image that is attached to this Server. Null if no ISO is attached. | getIso(): ?Iso2 | setIso(?Iso2 iso): void |
| `labels` | `array<string,string>` | Required | User-defined labels (key-value pairs) | getLabels(): array | setLabels(array labels): void |
| `loadBalancers` | `?(int[])` | Optional | - | getLoadBalancers(): ?array | setLoadBalancers(?array loadBalancers): void |
| `locked` | `bool` | Required | True if Server has been locked and is not available to user | getLocked(): bool | setLocked(bool locked): void |
| `name` | `string` | Required | Name of the Server (must be unique per Project and a valid hostname as per RFC 1123) | getName(): string | setName(string name): void |
| `outgoingTraffic` | `?float` | Required | Outbound Traffic for the current billing period in bytes | getOutgoingTraffic(): ?float | setOutgoingTraffic(?float outgoingTraffic): void |
| `placementGroup` | [`?PlacementGroupNullable`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/placement-group-nullable.md) | Optional | - | getPlacementGroup(): ?PlacementGroupNullable | setPlacementGroup(?PlacementGroupNullable placementGroup): void |
| `primaryDiskSize` | `float` | Required | Size of the primary Disk | getPrimaryDiskSize(): float | setPrimaryDiskSize(float primaryDiskSize): void |
| `privateNet` | [`PrivateNet4[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/private-net-4.md) | Required | Private networks information | getPrivateNet(): array | setPrivateNet(array privateNet): void |
| `protection` | [`Protection20`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/protection-20.md) | Required | Protection configuration for the Server | getProtection(): Protection20 | setProtection(Protection20 protection): void |
| `publicNet` | [`PublicNet4`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/public-net-4.md) | Required | Public network information. The Server's IPv4 address can be found in `public_net->ipv4->ip` | getPublicNet(): PublicNet4 | setPublicNet(PublicNet4 publicNet): void |
| `rescueEnabled` | `bool` | Required | True if rescue mode is enabled. Server will then boot into rescue system on next reboot | getRescueEnabled(): bool | setRescueEnabled(bool rescueEnabled): void |
| `serverType` | [`ServerType1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/server-type-1.md) | Required | Type of Server - determines how much ram, disk and cpu a Server has | getServerType(): ServerType1 | setServerType(ServerType1 serverType): void |
| `status` | [`string(Status73)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/enumerations/status-73.md) | Required | Status of the Server | getStatus(): string | setStatus(string status): void |
| `volumes` | `?(int[])` | Optional | IDs of Volumes assigned to this Server | getVolumes(): ?array | setVolumes(?array volumes): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
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

$server18 = Server18Builder::init(
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
        'key0' => 'labels4',
        'key1' => 'labels3',
        'key2' => 'labels2'
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
    Status73::RUNNING
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
            248
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
            199,
            200,
            201
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



