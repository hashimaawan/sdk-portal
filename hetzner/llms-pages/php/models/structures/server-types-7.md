# Server Types 7

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRlNlcnZlclR5cGVzNw


# Class Name

`ServerTypes7`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `cores` | `float` | Required | Number of cpu cores a Server of this type will have | getCores(): float | setCores(float cores): void |
| `cpuType` | [`string(CpuTypeEnum)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/enumerations/cpu-type.md) | Required | Type of cpu | getCpuType(): string | setCpuType(string cpuType): void |
| `deprecated` | `bool` | Required | True if Server type is deprecated | getDeprecated(): bool | setDeprecated(bool deprecated): void |
| `description` | `string` | Required | Description of the Server type | getDescription(): string | setDescription(string description): void |
| `disk` | `float` | Required | Disk size a Server of this type will have in GB | getDisk(): float | setDisk(float disk): void |
| `id` | `float` | Required | ID of the Server type | getId(): float | setId(float id): void |
| `memory` | `float` | Required | Memory a Server of this type will have in GB | getMemory(): float | setMemory(float memory): void |
| `name` | `string` | Required | Unique identifier of the Server type | getName(): string | setName(string name): void |
| `prices` | [`Price9[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/price-9.md) | Required | Prices in different Locations | getPrices(): array | setPrices(array prices): void |
| `storageType` | [`string(StorageTypeEnum)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/enumerations/storage-type.md) | Required | Type of Server boot drive. Local has higher speed. Network has better availability. | getStorageType(): string | setStorageType(string storageType): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\ServerTypes7Builder;
use HetznerCloudAPILib\Models\CpuTypeEnum;
use HetznerCloudAPILib\Models\Builders\Price9Builder;
use HetznerCloudAPILib\Models\Builders\PriceHourly8Builder;
use HetznerCloudAPILib\Models\Builders\PriceMonthly10Builder;
use HetznerCloudAPILib\Models\StorageTypeEnum;

$serverTypes7 = ServerTypes7Builder::init(
    1,
    CpuTypeEnum::SHARED,
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
            )->build(),
            PriceMonthly10Builder::init(
                '1.1900000000000000',
                '1.0000000000'
            )->build()
        )->build()
    ],
    StorageTypeEnum::LOCAL
)->build();
```



