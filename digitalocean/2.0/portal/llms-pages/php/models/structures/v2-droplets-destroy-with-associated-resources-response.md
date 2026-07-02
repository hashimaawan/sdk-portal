# V2 Droplets Destroy with Associated Resources Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBEcm9wbGV0cyUyNTIwRGVzdHJveSUyNTIwV2l0aCUyNTIwQXNzb2NpYXRlZCUyNTIwUmVzb3VyY2VzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2DropletsDestroyWithAssociatedResourcesResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `floatingIps` | [`?(FloatingIp[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/floating-ip.md) | Optional | - | getFloatingIps(): ?array | setFloatingIps(?array floatingIps): void |
| `reservedIps` | [`?(FloatingIp[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/floating-ip.md) | Optional | - | getReservedIps(): ?array | setReservedIps(?array reservedIps): void |
| `snapshots` | [`?(FloatingIp[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/floating-ip.md) | Optional | - | getSnapshots(): ?array | setSnapshots(?array snapshots): void |
| `volumeSnapshots` | [`?(FloatingIp[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/floating-ip.md) | Optional | - | getVolumeSnapshots(): ?array | setVolumeSnapshots(?array volumeSnapshots): void |
| `volumes` | [`?(FloatingIp[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/floating-ip.md) | Optional | - | getVolumes(): ?array | setVolumes(?array volumes): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2DropletsDestroyWithAssociatedResourcesResponseBuilder;
use DigitalOceanApiLib\Models\Builders\FloatingIpBuilder;
use DigitalOceanApiLib\ApiHelper;

$v2DropletsDestroyWithAssociatedResourcesResponse = V2DropletsDestroyWithAssociatedResourcesResponseBuilder::init()
    ->floatingIps(
        [
            FloatingIpBuilder::init()
                ->cost('cost0')
                ->id('id2')
                ->name('name2')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            FloatingIpBuilder::init()
                ->cost('cost0')
                ->id('id2')
                ->name('name2')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->reservedIps(
        [
            FloatingIpBuilder::init()
                ->cost('cost8')
                ->id('id0')
                ->name('name0')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->snapshots(
        [
            FloatingIpBuilder::init()
                ->cost('cost0')
                ->id('id2')
                ->name('name2')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            FloatingIpBuilder::init()
                ->cost('cost0')
                ->id('id2')
                ->name('name2')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->volumeSnapshots(
        [
            FloatingIpBuilder::init()
                ->cost('cost6')
                ->id('id8')
                ->name('name8')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->volumes(
        [
            FloatingIpBuilder::init()
                ->cost('cost4')
                ->id('id6')
                ->name('name6')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            FloatingIpBuilder::init()
                ->cost('cost4')
                ->id('id6')
                ->name('name6')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



