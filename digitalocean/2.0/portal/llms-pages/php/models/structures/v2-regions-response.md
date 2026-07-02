# V2 Regions Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBSZWdpb25zJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2RegionsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `regions` | [`Region[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/region.md) | Required | - | getRegions(): array | setRegions(array regions): void |
| `links` | [`?Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/links.md) | Optional | - | getLinks(): ?Links | setLinks(?Links links): void |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/meta.md) | Required | - | getMeta(): Meta | setMeta(Meta meta): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2RegionsResponseBuilder;
use DigitalOceanApiLib\Models\Builders\RegionBuilder;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Models\Builders\MetaBuilder;
use DigitalOceanApiLib\Models\Builders\LinksBuilder;
use DigitalOceanApiLib\Models\Builders\PagesBuilder;

$v2RegionsResponse = V2RegionsResponseBuilder::init(
    [
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
            ->build()
    ],
    MetaBuilder::init(
        13
    )
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build()
)
    ->links(
        LinksBuilder::init()
            ->pages(
                PagesBuilder::init()
                    ->last('https://api.digitalocean.com/v2/regions?page=13&per_page=1')
                    ->next('https://api.digitalocean.com/v2/regions?page=2&per_page=1')
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



