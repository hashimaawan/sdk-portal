# V2 Registry Tags Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBSZWdpc3RyeSUyNTIwVGFncyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2RegistryTagsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `tags` | [`?(LatestTag[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/latest-tag.md) | Optional | - | getTags(): ?array | setTags(?array tags): void |
| `links` | [`?Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/links.md) | Optional | - | getLinks(): ?Links | setLinks(?Links links): void |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/meta.md) | Required | - | getMeta(): Meta | setMeta(Meta meta): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2RegistryTagsResponseBuilder;
use DigitalOceanApiLib\Models\Builders\MetaBuilder;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Models\Builders\LatestTagBuilder;
use DigitalOceanApiLib\Utils\DateTimeHelper;
use DigitalOceanApiLib\Models\Builders\LinksBuilder;
use DigitalOceanApiLib\Models\Builders\PagesBuilder;

$v2RegistryTagsResponse = V2RegistryTagsResponseBuilder::init(
    MetaBuilder::init(
        1
    )
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build()
)
    ->tags(
        [
            LatestTagBuilder::init()
                ->compressedSizeBytes(2803255)
                ->manifestDigest('sha256:cb8a924afdf0229ef7515d9e5b3024e23b3eb03ddbba287f4a19c6ac90b8d221')
                ->registryName('example')
                ->repository('repo-1')
                ->sizeBytes(5861888)
                ->tag('latest')
                ->updatedAt(DateTimeHelper::fromRfc3339DateTime('2020-04-09T23:54:25Z'))
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



