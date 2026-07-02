# Repository

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlJlcG9zaXRvcnk

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Repository`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `latestTag` | [`?LatestTag`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/latest-tag.md) | Optional | - | getLatestTag(): ?LatestTag | setLatestTag(?LatestTag latestTag): void |
| `name` | `?string` | Optional | The name of the repository. | getName(): ?string | setName(?string name): void |
| `registryName` | `?string` | Optional | The name of the container registry. | getRegistryName(): ?string | setRegistryName(?string registryName): void |
| `tagCount` | `?int` | Optional | The number of tags in the repository. | getTagCount(): ?int | setTagCount(?int tagCount): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\RepositoryBuilder;
use DigitalOceanApiLib\Models\Builders\LatestTagBuilder;
use DigitalOceanApiLib\ApiHelper;

$repository = RepositoryBuilder::init()
    ->latestTag(
        LatestTagBuilder::init()
            ->compressedSizeBytes(108)
            ->manifestDigest('manifest_digest2')
            ->registryName('registry_name4')
            ->repository('repository4')
            ->sizeBytes(226)
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->name('repo-1')
    ->registryName('example')
    ->tagCount(1)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



