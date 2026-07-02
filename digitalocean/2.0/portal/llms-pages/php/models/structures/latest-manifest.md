# Latest Manifest

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkxhdGVzdE1hbmlmZXN0

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`LatestManifest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `blobs` | [`?(Blob[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/blob.md) | Optional | All blobs associated with this manifest | getBlobs(): ?array | setBlobs(?array blobs): void |
| `compressedSizeBytes` | `?int` | Optional | The compressed size of the manifest in bytes. | getCompressedSizeBytes(): ?int | setCompressedSizeBytes(?int compressedSizeBytes): void |
| `digest` | `?string` | Optional | The manifest digest | getDigest(): ?string | setDigest(?string digest): void |
| `registryName` | `?string` | Optional | The name of the container registry. | getRegistryName(): ?string | setRegistryName(?string registryName): void |
| `repository` | `?string` | Optional | The name of the repository. | getRepository(): ?string | setRepository(?string repository): void |
| `sizeBytes` | `?int` | Optional | The uncompressed size of the manifest in bytes (this size is calculated asynchronously so it may not be immediately available). | getSizeBytes(): ?int | setSizeBytes(?int sizeBytes): void |
| `tags` | `?(string[])` | Optional | All tags associated with this manifest | getTags(): ?array | setTags(?array tags): void |
| `updatedAt` | `?DateTime` | Optional | The time the manifest was last updated. | getUpdatedAt(): ?\DateTime | setUpdatedAt(?\DateTime updatedAt): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\LatestManifestBuilder;
use DigitalOceanApiLib\Models\Builders\BlobBuilder;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Utils\DateTimeHelper;

$latestManifest = LatestManifestBuilder::init()
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
                ->build()
        ]
    )
    ->compressedSizeBytes(2803255)
    ->digest('sha256:cb8a924afdf0229ef7515d9e5b3024e23b3eb03ddbba287f4a19c6ac90b8d221')
    ->registryName('example')
    ->repository('repo-1')
    ->sizeBytes(5861888)
    ->tags(
        [
            'latest',
            'v1',
            'v2'
        ]
    )
    ->updatedAt(DateTimeHelper::fromRfc3339DateTime('2020-04-09T23:54:25Z'))
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



