# V2 Registry Garbage Collection Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBSZWdpc3RyeSUyNTIwR2FyYmFnZSUyNTIwQ29sbGVjdGlvbiUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2RegistryGarbageCollectionResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `garbageCollection` | [`?GarbageCollection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/garbage-collection.md) | Optional | - | getGarbageCollection(): ?GarbageCollection | setGarbageCollection(?GarbageCollection garbageCollection): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2RegistryGarbageCollectionResponseBuilder;
use DigitalOceanApiLib\Models\Builders\GarbageCollectionBuilder;
use DigitalOceanApiLib\Utils\DateTimeHelper;
use DigitalOceanApiLib\Models\Status15;
use DigitalOceanApiLib\ApiHelper;

$v2RegistryGarbageCollectionResponse = V2RegistryGarbageCollectionResponseBuilder::init()
    ->garbageCollection(
        GarbageCollectionBuilder::init()
            ->blobsDeleted(40)
            ->createdAt(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
            ->freedBytes(86)
            ->registryName('registry_name6')
            ->status(Status15::SUCCEEDED)
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



