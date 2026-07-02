# Registry

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlJlZ2lzdHJ5

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Registry`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `createdAt` | `?DateTime` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the registry was created. | getCreatedAt(): ?\DateTime | setCreatedAt(?\DateTime createdAt): void |
| `name` | `?string` | Optional | A globally unique name for the container registry. Must be lowercase and be composed only of numbers, letters and `-`, up to a limit of 63 characters.<br><br>**Constraints**: *Maximum Length*: `63`, *Pattern*: `^[a-z0-9-]{1,63}$` | getName(): ?string | setName(?string name): void |
| `region` | `?string` | Optional | Slug of the region where registry data is stored | getRegion(): ?string | setRegion(?string region): void |
| `storageUsageBytes` | `?int` | Optional, Read-only | The amount of storage used in the registry in bytes. | getStorageUsageBytes(): ?int | setStorageUsageBytes(?int storageUsageBytes): void |
| `storageUsageBytesUpdatedAt` | `?DateTime` | Optional, Read-only | The time at which the storage usage was updated. Storage usage is calculated asynchronously, and may not immediately reflect pushes to the registry. | getStorageUsageBytesUpdatedAt(): ?\DateTime | setStorageUsageBytesUpdatedAt(?\DateTime storageUsageBytesUpdatedAt): void |
| `subscription` | [`?Subscription`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/subscription.md) | Optional | - | getSubscription(): ?Subscription | setSubscription(?Subscription subscription): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\RegistryBuilder;
use DigitalOceanApiLib\Utils\DateTimeHelper;
use DigitalOceanApiLib\ApiHelper;

$registry = RegistryBuilder::init()
    ->createdAt(DateTimeHelper::fromRfc3339DateTime('2020-03-21T16:02:37Z'))
    ->name('example')
    ->region('fra1')
    ->storageUsageBytes(29393920)
    ->storageUsageBytesUpdatedAt(DateTimeHelper::fromRfc3339DateTime('2020-11-04T21:39:49.530562231Z'))
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



