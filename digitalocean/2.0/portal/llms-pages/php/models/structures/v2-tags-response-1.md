# V2 Tags Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBUYWdzJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2TagsResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `tag` | [`?Tag`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/tag.md) | Optional | A tag is a label that can be applied to a resource (currently Droplets, Images, Volumes, Volume Snapshots, and Database clusters) in order to better organize or facilitate the lookups and actions on it.<br>Tags have two attributes: a user defined `name` attribute and an embedded `resources` attribute with information about resources that have been tagged. | getTag(): ?Tag | setTag(?Tag tag): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2TagsResponse1Builder;
use DigitalOceanApiLib\Models\Builders\TagBuilder;
use DigitalOceanApiLib\Models\Builders\Resources2Builder;
use DigitalOceanApiLib\Models\Builders\DatabasesBuilder;
use DigitalOceanApiLib\ApiHelper;

$v2TagsResponse1 = V2TagsResponse1Builder::init()
    ->tag(
        TagBuilder::init()
            ->name('extra-awesome')
            ->resources(
                Resources2Builder::init()
                    ->count(0)
                    ->lastTaggedUri('last_tagged_uri6')
                    ->databases(
                        DatabasesBuilder::init()
                            ->count(0)
                            ->lastTaggedUri('last_tagged_uri2')
                            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                            ->build()
                    )
                    ->droplets(
                        DatabasesBuilder::init()
                            ->count(0)
                            ->lastTaggedUri('last_tagged_uri6')
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
                            ->count(0)
                            ->build()
                    )
                    ->volumes(
                        DatabasesBuilder::init()
                            ->count(0)
                            ->build()
                    )
                    ->additionalProperty('images', ApiHelper::deserialize('{"count":0}'))
                    ->build()
            )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



