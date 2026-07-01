# Server Types 7

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlNlcnZlclR5cGVzNw

*This model accepts additional fields of type array.*


# Class Name

`ServerTypes7`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `cores` | `float` | Required | Number of cpu cores a Server of this type will have | getCores(): float | setCores(float cores): void |
| `cpuType` | [`string(CpuType)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/enumerations/cpu-type.md) | Required | Type of cpu | getCpuType(): string | setCpuType(string cpuType): void |
| `deprecated` | `bool` | Required | True if Server type is deprecated | getDeprecated(): bool | setDeprecated(bool deprecated): void |
| `description` | `string` | Required | Description of the Server type | getDescription(): string | setDescription(string description): void |
| `disk` | `float` | Required | Disk size a Server of this type will have in GB | getDisk(): float | setDisk(float disk): void |
| `id` | `float` | Required | ID of the Server type | getId(): float | setId(float id): void |
| `memory` | `float` | Required | Memory a Server of this type will have in GB | getMemory(): float | setMemory(float memory): void |
| `name` | `string` | Required | Unique identifier of the Server type | getName(): string | setName(string name): void |
| `prices` | [`Price9[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/price-9.md) | Required | Prices in different Locations | getPrices(): array | setPrices(array prices): void |
| `storageType` | [`string(StorageType)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/enumerations/storage-type.md) | Required | Type of Server boot drive. Local has higher speed. Network has better availability. | getStorageType(): string | setStorageType(string storageType): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\ServerTypes7Builder;
use HetznerCloudApiLib\Models\CpuType;
use HetznerCloudApiLib\Models\Builders\Price9Builder;
use HetznerCloudApiLib\Models\Builders\PriceHourly8Builder;
use HetznerCloudApiLib\ApiHelper;
use HetznerCloudApiLib\Models\Builders\PriceMonthly10Builder;
use HetznerCloudApiLib\Models\StorageType;

$serverTypes7 = ServerTypes7Builder::init(
    1,
    CpuType::SHARED,
    false,
    'CX11',
    24,
    1,
    1,
    'cx11',
    [
        Price9Builder::init(
            'fsn1',
            PriceHourly8Builder::init(
                '1.1900000000000000',
                '1.0000000000'
            )
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            PriceMonthly10Builder::init(
                '1.1900000000000000',
                '1.0000000000'
            )
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    ],
    StorageType::LOCAL
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



