# V2 Volumes Actions Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBWb2x1bWVzJTI1MjBBY3Rpb25zJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2VolumesActionsResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `actions` | [`?(Action4[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/action-4.md) | Optional | - | getActions(): ?array | setActions(?array actions): void |
| `links` | [`?Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/links.md) | Optional | - | getLinks(): ?Links | setLinks(?Links links): void |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/meta.md) | Required | - | getMeta(): Meta | setMeta(Meta meta): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2VolumesActionsResponse1Builder;
use DigitalOceanApiLib\Models\Builders\MetaBuilder;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Models\Builders\Action4Builder;
use DigitalOceanApiLib\Utils\DateTimeHelper;
use DigitalOceanApiLib\Models\Builders\RegionBuilder;
use DigitalOceanApiLib\Models\Status1;
use DigitalOceanApiLib\Models\Builders\LinksBuilder;
use DigitalOceanApiLib\Models\Builders\PagesBuilder;

$v2VolumesActionsResponse1 = V2VolumesActionsResponse1Builder::init(
    MetaBuilder::init(
        1
    )
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build()
)
    ->actions(
        [
            Action4Builder::init()
                ->resourceId(238)
                ->type('attach_volume')
                ->completedAt(DateTimeHelper::fromRfc3339DateTime('2020-11-21T21:51:09Z'))
                ->id(72531856)
                ->region(
                    RegionBuilder::init(
                        true,
                        [
                            'private_networking',
                            'backups',
                            'ipv6',
                            'metadata'
                        ],
                        'New York 1',
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
                            's-32vcpu-192gb'
                        ],
                        'nyc1'
                    )
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                )
                ->regionSlug('nyc1')
                ->resourceType('volume')
                ->startedAt(DateTimeHelper::fromRfc3339DateTime('2020-11-21T21:51:09Z'))
                ->status(Status1::COMPLETED)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->links(
        LinksBuilder::init()
            ->pages(
                PagesBuilder::init()
                    ->last('last6')
                    ->next('next2')
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



