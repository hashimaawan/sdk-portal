# V2 Projects Default Resources Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBQcm9qZWN0cyUyNTIwRGVmYXVsdCUyNTIwUmVzb3VyY2VzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2ProjectsDefaultResourcesResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `resources` | [`?(Resources1[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/resources-1.md) | Optional | - | getResources(): ?array | setResources(?array resources): void |
| `links` | [`?Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/links.md) | Optional | - | getLinks(): ?Links | setLinks(?Links links): void |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/meta.md) | Required | - | getMeta(): Meta | setMeta(Meta meta): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2ProjectsDefaultResourcesResponseBuilder;
use DigitalOceanApiLib\Models\Builders\MetaBuilder;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Models\Builders\Resources1Builder;
use DigitalOceanApiLib\Utils\DateTimeHelper;
use DigitalOceanApiLib\Models\Builders\Links4Builder;
use DigitalOceanApiLib\Models\Status14;
use DigitalOceanApiLib\Models\Builders\LinksBuilder;
use DigitalOceanApiLib\Models\Builders\PagesBuilder;

$v2ProjectsDefaultResourcesResponse = V2ProjectsDefaultResourcesResponseBuilder::init(
    MetaBuilder::init(
        2
    )
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build()
)
    ->resources(
        [
            Resources1Builder::init()
                ->assignedAt(DateTimeHelper::fromRfc3339DateTime('2018-09-28T19:26:37Z'))
                ->links(
                    Links4Builder::init()
                        ->self('https://api.digitalocean.com/v2/droplets/13457723')
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                )
                ->status(Status14::OK)
                ->urn('do:droplet:13457723')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            Resources1Builder::init()
                ->assignedAt(DateTimeHelper::fromRfc3339DateTime('2019-03-31T16:24:14Z'))
                ->links(
                    Links4Builder::init()
                        ->self('https://api.digitalocean.com/v2/domains/example.com')
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                )
                ->status(Status14::OK)
                ->urn('do:domain:example.com')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->links(
        LinksBuilder::init()
            ->pages(
                PagesBuilder::init()
                    ->last('https://api.digitalocean.com/v2/projects/4e1bfbc3-dc3e-41f2-a18f-1b4d7ba71679/resources?page=1')
                    ->next('next2')
                    ->additionalProperty('first', ApiHelper::deserialize('"https://api.digitalocean.com/v2/projects/4e1bfbc3-dc3e-41f2-a18f-1b4d7ba71679/resources?page=1"'))
                    ->build()
            )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



