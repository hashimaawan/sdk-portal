# V2 Droplets Destroy with Associated Resources Status Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBEcm9wbGV0cyUyNTIwRGVzdHJveSUyNTIwV2l0aCUyNTIwQXNzb2NpYXRlZCUyNTIwUmVzb3VyY2VzJTI1MjBTdGF0dXMlMjUyMFJlc3BvbnNl

An objects containing information about a resources scheduled for deletion.

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2DropletsDestroyWithAssociatedResourcesStatusResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `completedAt` | `?DateTime` | Optional | A time value given in ISO8601 combined date and time format indicating when the requested action was completed. | getCompletedAt(): ?\DateTime | setCompletedAt(?\DateTime completedAt): void |
| `droplet` | [`?Droplet1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/droplet-1.md) | Optional | An object containing information about a resource scheduled for deletion. | getDroplet(): ?Droplet1 | setDroplet(?Droplet1 droplet): void |
| `failures` | `?int` | Optional | A count of the associated resources that failed to be destroyed, if any. | getFailures(): ?int | setFailures(?int failures): void |
| `resources` | [`?Resources`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/resources.md) | Optional | An object containing additional information about resource related to a Droplet requested to be destroyed. | getResources(): ?Resources | setResources(?Resources resources): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2DropletsDestroyWithAssociatedResourcesStatusResponseBuilder;
use DigitalOceanApiLib\Utils\DateTimeHelper;
use DigitalOceanApiLib\Models\Builders\Droplet1Builder;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Models\Builders\ResourcesBuilder;

$v2DropletsDestroyWithAssociatedResourcesStatusResponse = V2DropletsDestroyWithAssociatedResourcesStatusResponseBuilder::init()
    ->completedAt(DateTimeHelper::fromRfc3339DateTime('2020-04-01T18:11:49Z'))
    ->droplet(
        Droplet1Builder::init()
            ->destroyedAt(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
            ->errorMessage('error_message2')
            ->id('id0')
            ->name('name0')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->failures(0)
    ->resources(
        ResourcesBuilder::init()
            ->floatingIps(
                [
                    Droplet1Builder::init()
                        ->destroyedAt(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                        ->errorMessage('error_message4')
                        ->id('id2')
                        ->name('name2')
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build(),
                    Droplet1Builder::init()
                        ->destroyedAt(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                        ->errorMessage('error_message4')
                        ->id('id2')
                        ->name('name2')
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build(),
                    Droplet1Builder::init()
                        ->destroyedAt(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                        ->errorMessage('error_message4')
                        ->id('id2')
                        ->name('name2')
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                ]
            )
            ->reservedIps(
                [
                    Droplet1Builder::init()
                        ->destroyedAt(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                        ->errorMessage('error_message2')
                        ->id('id0')
                        ->name('name0')
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build(),
                    Droplet1Builder::init()
                        ->destroyedAt(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                        ->errorMessage('error_message2')
                        ->id('id0')
                        ->name('name0')
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                ]
            )
            ->snapshots(
                [
                    Droplet1Builder::init()
                        ->destroyedAt(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                        ->errorMessage('error_message4')
                        ->id('id2')
                        ->name('name2')
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build(),
                    Droplet1Builder::init()
                        ->destroyedAt(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                        ->errorMessage('error_message4')
                        ->id('id2')
                        ->name('name2')
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build(),
                    Droplet1Builder::init()
                        ->destroyedAt(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                        ->errorMessage('error_message4')
                        ->id('id2')
                        ->name('name2')
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                ]
            )
            ->volumeSnapshots(
                [
                    Droplet1Builder::init()
                        ->destroyedAt(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                        ->errorMessage('error_message0')
                        ->id('id8')
                        ->name('name8')
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build(),
                    Droplet1Builder::init()
                        ->destroyedAt(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                        ->errorMessage('error_message0')
                        ->id('id8')
                        ->name('name8')
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                ]
            )
            ->volumes(
                [
                    Droplet1Builder::init()
                        ->destroyedAt(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                        ->errorMessage('error_message8')
                        ->id('id6')
                        ->name('name6')
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                ]
            )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



