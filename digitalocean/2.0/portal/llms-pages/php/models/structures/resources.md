# Resources

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlJlc291cmNlcw

An object containing additional information about resource related to a Droplet requested to be destroyed.

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Resources`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `floatingIps` | [`?(Droplet1[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/droplet-1.md) | Optional | - | getFloatingIps(): ?array | setFloatingIps(?array floatingIps): void |
| `reservedIps` | [`?(Droplet1[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/droplet-1.md) | Optional | - | getReservedIps(): ?array | setReservedIps(?array reservedIps): void |
| `snapshots` | [`?(Droplet1[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/droplet-1.md) | Optional | - | getSnapshots(): ?array | setSnapshots(?array snapshots): void |
| `volumeSnapshots` | [`?(Droplet1[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/droplet-1.md) | Optional | - | getVolumeSnapshots(): ?array | setVolumeSnapshots(?array volumeSnapshots): void |
| `volumes` | [`?(Droplet1[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/droplet-1.md) | Optional | - | getVolumes(): ?array | setVolumes(?array volumes): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\ResourcesBuilder;
use DigitalOceanApiLib\Models\Builders\Droplet1Builder;
use DigitalOceanApiLib\Utils\DateTimeHelper;
use DigitalOceanApiLib\ApiHelper;

$resources = ResourcesBuilder::init()
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
    ->build();
```



