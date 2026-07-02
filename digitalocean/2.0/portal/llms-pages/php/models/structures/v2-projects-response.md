# V2 Projects Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBQcm9qZWN0cyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2ProjectsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `projects` | [`?(Project[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/project.md) | Optional | - | getProjects(): ?array | setProjects(?array projects): void |
| `links` | [`?Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/links.md) | Optional | - | getLinks(): ?Links | setLinks(?Links links): void |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/meta.md) | Required | - | getMeta(): Meta | setMeta(Meta meta): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2ProjectsResponseBuilder;
use DigitalOceanApiLib\Models\Builders\MetaBuilder;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Models\Builders\ProjectBuilder;
use DigitalOceanApiLib\Utils\DateTimeHelper;
use DigitalOceanApiLib\Models\Environment;
use DigitalOceanApiLib\Models\Builders\LinksBuilder;
use DigitalOceanApiLib\Models\Builders\PagesBuilder;

$v2ProjectsResponse = V2ProjectsResponseBuilder::init(
    MetaBuilder::init(
        2
    )
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build()
)
    ->projects(
        [
            ProjectBuilder::init()
                ->createdAt(DateTimeHelper::fromRfc3339DateTime('2018-09-27T20:10:35Z'))
                ->description('My website API')
                ->environment(Environment::PRODUCTION)
                ->id('4e1bfbc3-dc3e-41f2-a18f-1b4d7ba71679')
                ->name('my-web-api')
                ->ownerId(258992)
                ->ownerUuid('99525febec065ca37b2ffe4f852fd2b2581895e7')
                ->purpose('Service or API')
                ->updatedAt(DateTimeHelper::fromRfc3339DateTime('2018-09-27T20:10:35Z'))
                ->isDefault(false)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            ProjectBuilder::init()
                ->createdAt(DateTimeHelper::fromRfc3339DateTime('2017-10-19T21:44:20Z'))
                ->description('Default project')
                ->environment(Environment::DEVELOPMENT)
                ->id('addb4547-6bab-419a-8542-76263a033cf6')
                ->name('Default')
                ->ownerId(258992)
                ->ownerUuid('99525febec065ca37b2ffe4f852fd2b2581895e7')
                ->purpose('Just trying out DigitalOcean')
                ->updatedAt(DateTimeHelper::fromRfc3339DateTime('2019-11-05T18:50:03Z'))
                ->isDefault(true)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->links(
        LinksBuilder::init()
            ->pages(
                PagesBuilder::init()
                    ->last('https://api.digitalocean.com/v2/projects?page=1')
                    ->next('next2')
                    ->additionalProperty('first', ApiHelper::deserialize('"https://api.digitalocean.com/v2/projects?page=1"'))
                    ->build()
            )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



