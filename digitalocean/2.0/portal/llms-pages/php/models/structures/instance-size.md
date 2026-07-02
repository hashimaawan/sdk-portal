# Instance Size

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkluc3RhbmNlU2l6ZQ

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`InstanceSize`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `cpuType` | [`?string(MSharedSharedVcpuCoresDedicatedDedicatedVcpuCores)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/shared-shared-v-cpu-cores-dedicated-dedicated-v-cpu-cores.md) | Optional | **Default**: `MSharedSharedVcpuCoresDedicatedDedicatedVcpuCores::UNSPECIFIED` | getCpuType(): ?string | setCpuType(?string cpuType): void |
| `cpus` | `?string` | Optional | - | getCpus(): ?string | setCpus(?string cpus): void |
| `memoryBytes` | `?string` | Optional | - | getMemoryBytes(): ?string | setMemoryBytes(?string memoryBytes): void |
| `name` | `?string` | Optional | - | getName(): ?string | setName(?string name): void |
| `slug` | `?string` | Optional | - | getSlug(): ?string | setSlug(?string slug): void |
| `tierDowngradeTo` | `?string` | Optional | - | getTierDowngradeTo(): ?string | setTierDowngradeTo(?string tierDowngradeTo): void |
| `tierSlug` | `?string` | Optional | - | getTierSlug(): ?string | setTierSlug(?string tierSlug): void |
| `tierUpgradeTo` | `?string` | Optional | - | getTierUpgradeTo(): ?string | setTierUpgradeTo(?string tierUpgradeTo): void |
| `usdPerMonth` | `?string` | Optional | - | getUsdPerMonth(): ?string | setUsdPerMonth(?string usdPerMonth): void |
| `usdPerSecond` | `?string` | Optional | - | getUsdPerSecond(): ?string | setUsdPerSecond(?string usdPerSecond): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\InstanceSizeBuilder;
use DigitalOceanApiLib\Models\MSharedSharedVcpuCoresDedicatedDedicatedVcpuCores;
use DigitalOceanApiLib\ApiHelper;

$instanceSize = InstanceSizeBuilder::init()
    ->cpuType(MSharedSharedVcpuCoresDedicatedDedicatedVcpuCores::SHARED)
    ->cpus('3')
    ->memoryBytes('1048')
    ->name('name')
    ->slug('basic')
    ->tierDowngradeTo('basic')
    ->tierSlug('basic')
    ->tierUpgradeTo('basic')
    ->usdPerMonth('23')
    ->usdPerSecond('0.00000001232')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



