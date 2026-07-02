# Repository 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlJlcG9zaXRvcnkx

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Repository1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `latestManifest` | [`?LatestManifest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/latest-manifest.md) | Optional | - | getLatestManifest(): ?LatestManifest | setLatestManifest(?LatestManifest latestManifest): void |
| `manifestCount` | `?int` | Optional | The number of manifests in the repository. | getManifestCount(): ?int | setManifestCount(?int manifestCount): void |
| `name` | `?string` | Optional | The name of the repository. | getName(): ?string | setName(?string name): void |
| `registryName` | `?string` | Optional | The name of the container registry. | getRegistryName(): ?string | setRegistryName(?string registryName): void |
| `tagCount` | `?int` | Optional | The number of tags in the repository. | getTagCount(): ?int | setTagCount(?int tagCount): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\Repository1Builder;
use DigitalOceanApiLib\Models\Builders\LatestManifestBuilder;
use DigitalOceanApiLib\Models\Builders\BlobBuilder;
use DigitalOceanApiLib\ApiHelper;

$repository1 = Repository1Builder::init()
    ->latestManifest(
        LatestManifestBuilder::init()
            ->blobs(
                [
                    BlobBuilder::init()
                        ->compressedSizeBytes(12)
                        ->digest('digest2')
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build(),
                    BlobBuilder::init()
                        ->compressedSizeBytes(12)
                        ->digest('digest2')
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build(),
                    BlobBuilder::init()
                        ->compressedSizeBytes(12)
                        ->digest('digest2')
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                ]
            )
            ->compressedSizeBytes(154)
            ->digest('digest0')
            ->registryName('registry_name4')
            ->repository('repository4')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->manifestCount(1)
    ->name('repo-1')
    ->registryName('example')
    ->tagCount(1)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



