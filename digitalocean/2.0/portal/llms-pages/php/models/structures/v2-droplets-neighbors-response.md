# V2 Droplets Neighbors Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBEcm9wbGV0cyUyNTIwTmVpZ2hib3JzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2DropletsNeighborsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `droplets` | [`?(Droplet[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/droplet.md) | Optional | - | getDroplets(): ?array | setDroplets(?array droplets): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2DropletsNeighborsResponseBuilder;
use DigitalOceanApiLib\Models\Builders\DropletBuilder;
use DigitalOceanApiLib\Utils\DateTimeHelper;
use DigitalOceanApiLib\Models\Builders\Image1Builder;
use DigitalOceanApiLib\Models\Distribution;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Models\Builders\NetworksBuilder;
use DigitalOceanApiLib\Models\Builders\V4Builder;
use DigitalOceanApiLib\Models\Type10;
use DigitalOceanApiLib\Models\Builders\V6Builder;
use DigitalOceanApiLib\Models\Type11;
use DigitalOceanApiLib\Models\Builders\RegionBuilder;
use DigitalOceanApiLib\Models\Builders\SizeBuilder;
use DigitalOceanApiLib\Models\Status8;
use DigitalOceanApiLib\Models\Builders\KernelBuilder;
use DigitalOceanApiLib\Models\Builders\NextBackupWindowBuilder;

$v2DropletsNeighborsResponse = V2DropletsNeighborsResponseBuilder::init()
    ->droplets(
        [
            DropletBuilder::init(
                [
                    104,
                    105
                ],
                DateTimeHelper::fromRfc3339DateTimeRequired('2016-03-13T12:52:32.123Z'),
                98,
                [
                    'features1',
                    'features2',
                    'features3'
                ],
                232,
                Image1Builder::init()
                    ->createdAt(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                    ->description('description6')
                    ->distribution(Distribution::COREOS)
                    ->errorMessage('error_message8')
                    ->id(128)
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build(),
                false,
                16,
                'name0',
                NetworksBuilder::init()
                    ->v4(
                        [
                            V4Builder::init()
                                ->gateway('gateway2')
                                ->ipAddress('ip_address2')
                                ->netmask('netmask2')
                                ->type(Type10::PUBLIC_)
                                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                ->build(),
                            V4Builder::init()
                                ->gateway('gateway2')
                                ->ipAddress('ip_address2')
                                ->netmask('netmask2')
                                ->type(Type10::PUBLIC_)
                                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                ->build(),
                            V4Builder::init()
                                ->gateway('gateway2')
                                ->ipAddress('ip_address2')
                                ->netmask('netmask2')
                                ->type(Type10::PUBLIC_)
                                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                ->build()
                        ]
                    )
                    ->v6(
                        [
                            V6Builder::init()
                                ->gateway('gateway4')
                                ->ipAddress('ip_address4')
                                ->netmask(106)
                                ->type(Type11::PUBLIC_)
                                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                ->build(),
                            V6Builder::init()
                                ->gateway('gateway4')
                                ->ipAddress('ip_address4')
                                ->netmask(106)
                                ->type(Type11::PUBLIC_)
                                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                ->build()
                        ]
                    )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build(),
                RegionBuilder::init(
                    false,
                    [
                        'features7',
                        'features8',
                        'features9'
                    ],
                    'name6',
                    [
                        'sizes6'
                    ],
                    'slug0'
                )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build(),
                SizeBuilder::init(
                    false,
                    'description0',
                    252,
                    168,
                    121.04,
                    162.04,
                    [
                        'regions5'
                    ],
                    'slug6',
                    150.78,
                    234
                )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build(),
                'size_slug0',
                [
                    93,
                    94
                ],
                Status8::NEW_,
                [
                    'tags5'
                ],
                80,
                [
                    'volume_ids0',
                    'volume_ids1',
                    'volume_ids2'
                ]
            )
                ->kernel(
                    KernelBuilder::init()
                        ->id(16)
                        ->name('name4')
                        ->version('version0')
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                )
                ->nextBackupWindow(
                    NextBackupWindowBuilder::init()
                        ->end(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                        ->start(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                )
                ->vpcUuid('vpc_uuid0')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            DropletBuilder::init(
                [
                    104,
                    105
                ],
                DateTimeHelper::fromRfc3339DateTimeRequired('2016-03-13T12:52:32.123Z'),
                98,
                [
                    'features1',
                    'features2',
                    'features3'
                ],
                232,
                Image1Builder::init()
                    ->createdAt(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                    ->description('description6')
                    ->distribution(Distribution::COREOS)
                    ->errorMessage('error_message8')
                    ->id(128)
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build(),
                false,
                16,
                'name0',
                NetworksBuilder::init()
                    ->v4(
                        [
                            V4Builder::init()
                                ->gateway('gateway2')
                                ->ipAddress('ip_address2')
                                ->netmask('netmask2')
                                ->type(Type10::PUBLIC_)
                                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                ->build(),
                            V4Builder::init()
                                ->gateway('gateway2')
                                ->ipAddress('ip_address2')
                                ->netmask('netmask2')
                                ->type(Type10::PUBLIC_)
                                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                ->build(),
                            V4Builder::init()
                                ->gateway('gateway2')
                                ->ipAddress('ip_address2')
                                ->netmask('netmask2')
                                ->type(Type10::PUBLIC_)
                                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                ->build()
                        ]
                    )
                    ->v6(
                        [
                            V6Builder::init()
                                ->gateway('gateway4')
                                ->ipAddress('ip_address4')
                                ->netmask(106)
                                ->type(Type11::PUBLIC_)
                                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                ->build(),
                            V6Builder::init()
                                ->gateway('gateway4')
                                ->ipAddress('ip_address4')
                                ->netmask(106)
                                ->type(Type11::PUBLIC_)
                                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                ->build()
                        ]
                    )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build(),
                RegionBuilder::init(
                    false,
                    [
                        'features7',
                        'features8',
                        'features9'
                    ],
                    'name6',
                    [
                        'sizes6'
                    ],
                    'slug0'
                )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build(),
                SizeBuilder::init(
                    false,
                    'description0',
                    252,
                    168,
                    121.04,
                    162.04,
                    [
                        'regions5'
                    ],
                    'slug6',
                    150.78,
                    234
                )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build(),
                'size_slug0',
                [
                    93,
                    94
                ],
                Status8::NEW_,
                [
                    'tags5'
                ],
                80,
                [
                    'volume_ids0',
                    'volume_ids1',
                    'volume_ids2'
                ]
            )
                ->kernel(
                    KernelBuilder::init()
                        ->id(16)
                        ->name('name4')
                        ->version('version0')
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                )
                ->nextBackupWindow(
                    NextBackupWindowBuilder::init()
                        ->end(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                        ->start(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                )
                ->vpcUuid('vpc_uuid0')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            DropletBuilder::init(
                [
                    104,
                    105
                ],
                DateTimeHelper::fromRfc3339DateTimeRequired('2016-03-13T12:52:32.123Z'),
                98,
                [
                    'features1',
                    'features2',
                    'features3'
                ],
                232,
                Image1Builder::init()
                    ->createdAt(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                    ->description('description6')
                    ->distribution(Distribution::COREOS)
                    ->errorMessage('error_message8')
                    ->id(128)
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build(),
                false,
                16,
                'name0',
                NetworksBuilder::init()
                    ->v4(
                        [
                            V4Builder::init()
                                ->gateway('gateway2')
                                ->ipAddress('ip_address2')
                                ->netmask('netmask2')
                                ->type(Type10::PUBLIC_)
                                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                ->build(),
                            V4Builder::init()
                                ->gateway('gateway2')
                                ->ipAddress('ip_address2')
                                ->netmask('netmask2')
                                ->type(Type10::PUBLIC_)
                                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                ->build(),
                            V4Builder::init()
                                ->gateway('gateway2')
                                ->ipAddress('ip_address2')
                                ->netmask('netmask2')
                                ->type(Type10::PUBLIC_)
                                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                ->build()
                        ]
                    )
                    ->v6(
                        [
                            V6Builder::init()
                                ->gateway('gateway4')
                                ->ipAddress('ip_address4')
                                ->netmask(106)
                                ->type(Type11::PUBLIC_)
                                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                ->build(),
                            V6Builder::init()
                                ->gateway('gateway4')
                                ->ipAddress('ip_address4')
                                ->netmask(106)
                                ->type(Type11::PUBLIC_)
                                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                ->build()
                        ]
                    )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build(),
                RegionBuilder::init(
                    false,
                    [
                        'features7',
                        'features8',
                        'features9'
                    ],
                    'name6',
                    [
                        'sizes6'
                    ],
                    'slug0'
                )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build(),
                SizeBuilder::init(
                    false,
                    'description0',
                    252,
                    168,
                    121.04,
                    162.04,
                    [
                        'regions5'
                    ],
                    'slug6',
                    150.78,
                    234
                )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build(),
                'size_slug0',
                [
                    93,
                    94
                ],
                Status8::NEW_,
                [
                    'tags5'
                ],
                80,
                [
                    'volume_ids0',
                    'volume_ids1',
                    'volume_ids2'
                ]
            )
                ->kernel(
                    KernelBuilder::init()
                        ->id(16)
                        ->name('name4')
                        ->version('version0')
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                )
                ->nextBackupWindow(
                    NextBackupWindowBuilder::init()
                        ->end(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                        ->start(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                )
                ->vpcUuid('vpc_uuid0')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



