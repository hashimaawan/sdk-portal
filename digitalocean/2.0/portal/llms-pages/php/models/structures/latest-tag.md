# Latest Tag

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkxhdGVzdFRhZw

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`LatestTag`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `compressedSizeBytes` | `?int` | Optional | The compressed size of the tag in bytes. | getCompressedSizeBytes(): ?int | setCompressedSizeBytes(?int compressedSizeBytes): void |
| `manifestDigest` | `?string` | Optional | The digest of the manifest associated with the tag. | getManifestDigest(): ?string | setManifestDigest(?string manifestDigest): void |
| `registryName` | `?string` | Optional | The name of the container registry. | getRegistryName(): ?string | setRegistryName(?string registryName): void |
| `repository` | `?string` | Optional | The name of the repository. | getRepository(): ?string | setRepository(?string repository): void |
| `sizeBytes` | `?int` | Optional | The uncompressed size of the tag in bytes (this size is calculated asynchronously so it may not be immediately available). | getSizeBytes(): ?int | setSizeBytes(?int sizeBytes): void |
| `tag` | `?string` | Optional | The name of the tag. | getTag(): ?string | setTag(?string tag): void |
| `updatedAt` | `?DateTime` | Optional | The time the tag was last updated. | getUpdatedAt(): ?\DateTime | setUpdatedAt(?\DateTime updatedAt): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\LatestTagBuilder;
use DigitalOceanApiLib\Utils\DateTimeHelper;
use DigitalOceanApiLib\ApiHelper;

$latestTag = LatestTagBuilder::init()
    ->compressedSizeBytes(2803255)
    ->manifestDigest('sha256:cb8a924afdf0229ef7515d9e5b3024e23b3eb03ddbba287f4a19c6ac90b8d221')
    ->registryName('example')
    ->repository('repo-1')
    ->sizeBytes(5861888)
    ->tag('latest')
    ->updatedAt(DateTimeHelper::fromRfc3339DateTime('2020-04-09T23:54:25Z'))
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



