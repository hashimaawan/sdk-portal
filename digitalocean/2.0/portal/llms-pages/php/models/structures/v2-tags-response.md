# V2 Tags Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBUYWdzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2TagsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `tags` | [`?(Tag[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/tag.md) | Optional | - | getTags(): ?array | setTags(?array tags): void |
| `links` | [`?Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/links.md) | Optional | - | getLinks(): ?Links | setLinks(?Links links): void |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/meta.md) | Required | - | getMeta(): Meta | setMeta(Meta meta): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2TagsResponseBuilder;
use DigitalOceanApiLib\Models\Builders\MetaBuilder;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Models\Builders\TagBuilder;
use DigitalOceanApiLib\Models\Builders\Resources2Builder;
use DigitalOceanApiLib\Models\Builders\DatabasesBuilder;
use DigitalOceanApiLib\Models\Builders\LinksBuilder;
use DigitalOceanApiLib\Models\Builders\PagesBuilder;

$v2TagsResponse = V2TagsResponseBuilder::init(
    MetaBuilder::init(
        1
    )
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build()
)
    ->tags(
        [
            TagBuilder::init()
                ->name('extra-awesome')
                ->resources(
                    Resources2Builder::init()
                        ->count(5)
                        ->lastTaggedUri('https://api.digitalocean.com/v2/images/7555620')
                        ->databases(
                            DatabasesBuilder::init()
                                ->count(1)
                                ->lastTaggedUri('https://api.digitalocean.com/v2/databases/b92438f6-ba03-416c-b642-e9236db91976')
                                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                ->build()
                        )
                        ->droplets(
                            DatabasesBuilder::init()
                                ->count(1)
                                ->lastTaggedUri('https://api.digitalocean.com/v2/droplets/3164444')
                                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                ->build()
                        )
                        ->imgages(
                            DatabasesBuilder::init()
                                ->count(158)
                                ->lastTaggedUri('last_tagged_uri4')
                                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                ->build()
                        )
                        ->volumeSnapshots(
                            DatabasesBuilder::init()
                                ->count(1)
                                ->lastTaggedUri('https://api.digitalocean.com/v2/snapshots/1f6f46e8-6b60-11e9-be4e-0a58ac144519')
                                ->build()
                        )
                        ->volumes(
                            DatabasesBuilder::init()
                                ->count(1)
                                ->lastTaggedUri('https://api.digitalocean.com/v2/volumes/3d80cb72-342b-4aaa-b92e-4e4abb24a933')
                                ->build()
                        )
                        ->additionalProperty('images', ApiHelper::deserialize('{"count":1,"last_tagged_uri":"https://api.digitalocean.com/v2/images/7555620"}'))
                        ->build()
                )
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



