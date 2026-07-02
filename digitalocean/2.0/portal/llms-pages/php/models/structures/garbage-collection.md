# Garbage Collection

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkdhcmJhZ2VDb2xsZWN0aW9u

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`GarbageCollection`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `blobsDeleted` | `?int` | Optional | The number of blobs deleted as a result of this garbage collection. | getBlobsDeleted(): ?int | setBlobsDeleted(?int blobsDeleted): void |
| `createdAt` | `?DateTime` | Optional | The time the garbage collection was created. | getCreatedAt(): ?\DateTime | setCreatedAt(?\DateTime createdAt): void |
| `freedBytes` | `?int` | Optional | The number of bytes freed as a result of this garbage collection. | getFreedBytes(): ?int | setFreedBytes(?int freedBytes): void |
| `registryName` | `?string` | Optional | The name of the container registry. | getRegistryName(): ?string | setRegistryName(?string registryName): void |
| `status` | [`?string(Status15)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/status-15.md) | Optional | The current status of this garbage collection. | getStatus(): ?string | setStatus(?string status): void |
| `updatedAt` | `?DateTime` | Optional | The time the garbage collection was last updated. | getUpdatedAt(): ?\DateTime | setUpdatedAt(?\DateTime updatedAt): void |
| `uuid` | `?string` | Optional | A string specifying the UUID of the garbage collection. | getUuid(): ?string | setUuid(?string uuid): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\GarbageCollectionBuilder;
use DigitalOceanApiLib\Utils\DateTimeHelper;
use DigitalOceanApiLib\Models\Status15;
use DigitalOceanApiLib\ApiHelper;

$garbageCollection = GarbageCollectionBuilder::init()
    ->blobsDeleted(42)
    ->createdAt(DateTimeHelper::fromRfc3339DateTime('2020-10-30T21:03:24Z'))
    ->freedBytes(667)
    ->registryName('example')
    ->status(Status15::REQUESTED)
    ->updatedAt(DateTimeHelper::fromRfc3339DateTime('2020-10-30T21:03:44Z'))
    ->uuid('eff0feee-49c7-4e8f-ba5c-a320c109c8a8')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



