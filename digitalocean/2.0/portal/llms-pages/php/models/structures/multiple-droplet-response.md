# Multiple Droplet Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRk11bHRpcGxlJTI1MjBEcm9wbGV0JTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`MultipleDropletResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `droplets` | [`Droplet[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/droplet.md) | Required | - | getDroplets(): array | setDroplets(array droplets): void |
| `links` | [`Links1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/links-1.md) | Required | - | getLinks(): Links1 | setLinks(Links1 links): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\MultipleDropletResponseBuilder;
use DigitalOceanApiLib\Models\Builders\DropletBuilder;
use DigitalOceanApiLib\Utils\DateTimeHelper;
use DigitalOceanApiLib\Models\Builders\Image1Builder;
use DigitalOceanApiLib\Models\Distribution;
use DigitalOceanApiLib\Models\Region2;
use DigitalOceanApiLib\Models\Status7;
use DigitalOceanApiLib\Models\Type9;
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
use DigitalOceanApiLib\Models\Builders\Links1Builder;
use DigitalOceanApiLib\Models\Builders\Action1Builder;

$multipleDropletResponse = MultipleDropletResponseBuilder::init(
    [
        DropletBuilder::init(
            [
                53893572
            ],
            DateTimeHelper::fromRfc3339DateTimeRequired('2020-07-21T18:37:44Z'),
            25,
            [
                'backups',
                'private_networking',
                'ipv6'
            ],
            3164444,
            Image1Builder::init()
                ->createdAt(DateTimeHelper::fromRfc3339DateTime('2020-05-04T22:23:02Z'))
                ->description('description6')
                ->distribution(Distribution::UBUNTU)
                ->errorMessage('error_message8')
                ->id(7555620)
                ->minDiskSize(20)
                ->name('Nifty New Snapshot')
                ->public(true)
                ->regions(
                    [
                        Region2::NYC1,
                        Region2::NYC2
                    ]
                )
                ->sizeGigabytes(2.34)
                ->slug('nifty1')
                ->status(Status7::NEW_)
                ->tags(
                    [
                        'base-image',
                        'prod'
                    ]
                )
                ->type(Type9::SNAPSHOT)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            false,
            1024,
            'example.com',
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
                true,
                [
                    'private_networking',
                    'backups',
                    'ipv6',
                    'metadata',
                    'install_agent',
                    'storage',
                    'image_transfer'
                ],
                'New York 3',
                [
                    's-1vcpu-1gb',
                    's-1vcpu-2gb',
                    's-1vcpu-3gb',
                    's-2vcpu-2gb',
                    's-3vcpu-1gb',
                    's-2vcpu-4gb',
                    's-4vcpu-8gb',
                    's-6vcpu-16gb',
                    's-8vcpu-32gb',
                    's-12vcpu-48gb',
                    's-16vcpu-64gb',
                    's-20vcpu-96gb',
                    's-24vcpu-128gb',
                    's-32vcpu-192g'
                ],
                'nyc3'
            )
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            SizeBuilder::init(
                true,
                'Basic',
                25,
                1024,
                0.00743999984115362,
                5,
                [
                    'ams2',
                    'ams3',
                    'blr1',
                    'fra1',
                    'lon1',
                    'nyc1',
                    'nyc2',
                    'nyc3',
                    'sfo1',
                    'sfo2',
                    'sfo3',
                    'sgp1',
                    'tor1'
                ],
                's-1vcpu-1gb',
                1,
                1
            )
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            's-1vcpu-1gb',
            [
                67512819
            ],
            Status8::ACTIVE,
            [
                'web',
                'env:prod'
            ],
            1,
            [
                '506f78a4-e098-11e5-ad9f-000f53306ae1'
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
                    ->end(DateTimeHelper::fromRfc3339DateTime('2019-12-04T23:00:00Z'))
                    ->start(DateTimeHelper::fromRfc3339DateTime('2019-12-04T00:00:00Z'))
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            )
            ->vpcUuid('760e09ef-dc84-11e8-981e-3cfdfeaae000')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    ],
    Links1Builder::init()
        ->actions(
            [
                Action1Builder::init()
                    ->href('href0')
                    ->id(154)
                    ->rel('rel4')
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            ]
        )
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build()
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



