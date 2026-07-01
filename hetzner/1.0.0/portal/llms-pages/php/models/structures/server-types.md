# Server Types

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlNlcnZlclR5cGVz

The Server types the Datacenter can handle

*This model accepts additional fields of type array.*


# Class Name

`ServerTypes`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `available` | `float[]` | Required | IDs of Server types that are supported and for which the Datacenter has enough resources left | getAvailable(): array | setAvailable(array available): void |
| `availableForMigration` | `float[]` | Required | IDs of Server types that are supported and for which the Datacenter has enough resources left | getAvailableForMigration(): array | setAvailableForMigration(array availableForMigration): void |
| `supported` | `float[]` | Required | IDs of Server types that are supported in the Datacenter | getSupported(): array | setSupported(array supported): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\ServerTypesBuilder;
use HetznerCloudApiLib\ApiHelper;

$serverTypes = ServerTypesBuilder::init(
    [
        1,
        2,
        3
    ],
    [
        1,
        2,
        3
    ],
    [
        1,
        2,
        3
    ]
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



