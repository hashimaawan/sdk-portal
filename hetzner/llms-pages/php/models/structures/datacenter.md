# Datacenter

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRkRhdGFjZW50ZXI


# Class Name

`Datacenter`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `description` | `string` | Required | Description of the Datacenter | getDescription(): string | setDescription(string description): void |
| `id` | `int` | Required | ID of the Resource | getId(): int | setId(int id): void |
| `location` | [`Location`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/location.md) | Required | - | getLocation(): Location | setLocation(Location location): void |
| `name` | `string` | Required | Unique identifier of the Datacenter | getName(): string | setName(string name): void |
| `serverTypes` | [`ServerTypes`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/server-types.md) | Required | The Server types the Datacenter can handle | getServerTypes(): ServerTypes | setServerTypes(ServerTypes serverTypes): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\DatacenterBuilder;
use HetznerCloudAPILib\Models\Builders\LocationBuilder;
use HetznerCloudAPILib\Models\Builders\ServerTypesBuilder;

$datacenter = DatacenterBuilder::init(
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
    )->build(),
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
    )->build()
)->build();
```



