# Datacenter 6

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkRhdGFjZW50ZXI2

Datacenter this Resource is located at

*This model accepts additional fields of type array.*


# Class Name

`Datacenter6`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `description` | `string` | Required | Description of the Datacenter | getDescription(): string | setDescription(string description): void |
| `id` | `int` | Required | ID of the Resource | getId(): int | setId(int id): void |
| `location` | [`Location`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/location.md) | Required | - | getLocation(): Location | setLocation(Location location): void |
| `name` | `string` | Required | Unique identifier of the Datacenter | getName(): string | setName(string name): void |
| `serverTypes` | [`ServerTypes`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/server-types.md) | Required | The Server types the Datacenter can handle | getServerTypes(): ServerTypes | setServerTypes(ServerTypes serverTypes): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\Datacenter6Builder;
use HetznerCloudApiLib\Models\Builders\LocationBuilder;
use HetznerCloudApiLib\ApiHelper;
use HetznerCloudApiLib\Models\Builders\ServerTypesBuilder;

$datacenter6 = Datacenter6Builder::init(
    'Falkenstein DC Park 8',
    42,
    LocationBuilder::init(
        'Falkenstein',
        'DE',
        'Falkenstein DC Park 1',
        1,
        50.47612,
        12.370071,
        'fsn1',
        'eu-central'
    )
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build(),
    'fsn1-dc8',
    ServerTypesBuilder::init(
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
        ->build()
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



