# V2 Apps Tiers Instance Sizes Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBUaWVycyUyNTIwSW5zdGFuY2UlMjUyMFNpemVzJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2AppsTiersInstanceSizesResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `instanceSize` | [`?InstanceSize`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/instance-size.md) | Optional | - | getInstanceSize(): ?InstanceSize | setInstanceSize(?InstanceSize instanceSize): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2AppsTiersInstanceSizesResponse1Builder;
use DigitalOceanApiLib\Models\Builders\InstanceSizeBuilder;
use DigitalOceanApiLib\Models\MSharedSharedVcpuCoresDedicatedDedicatedVcpuCores;
use DigitalOceanApiLib\ApiHelper;

$v2AppsTiersInstanceSizesResponse1 = V2AppsTiersInstanceSizesResponse1Builder::init()
    ->instanceSize(
        InstanceSizeBuilder::init()
            ->cpuType(MSharedSharedVcpuCoresDedicatedDedicatedVcpuCores::DEDICATED)
            ->cpus('cpus4')
            ->memoryBytes('memory_bytes8')
            ->name('name8')
            ->slug('slug2')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



