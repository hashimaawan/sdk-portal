# Volume 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlZvbHVtZTE


# Class Name

`Volume1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `created` | `string` | Required | Point in time when the Resource was created (in ISO-8601 format) | getCreated(): string | setCreated(string created): void |
| `format` | `?string` | Required | Filesystem of the Volume if formatted on creation, null if not formatted on creation | getFormat(): ?string | setFormat(?string format): void |
| `id` | `int` | Required | ID of the Resource | getId(): int | setId(int id): void |
| `labels` | `array<string,string>` | Required | User-defined labels (key-value pairs) | getLabels(): array | setLabels(array labels): void |
| `linuxDevice` | `string` | Required | Device path on the file system for the Volume | getLinuxDevice(): string | setLinuxDevice(string linuxDevice): void |
| `location` | [`Location16`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/location-16.md) | Required | Location of the Volume. Volume can only be attached to Servers in the same Location. | getLocation(): Location16 | setLocation(Location16 location): void |
| `name` | `string` | Required | Name of the Resource. Must be unique per Project. | getName(): string | setName(string name): void |
| `protection` | [`Protection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/protection.md) | Required | Protection configuration for the Resource | getProtection(): Protection | setProtection(Protection protection): void |
| `server` | `?int` | Required | ID of the Server the Volume is attached to, null if it is not attached at all | getServer(): ?int | setServer(?int server): void |
| `size` | `float` | Required | Size in GB of the Volume | getSize(): float | setSize(float size): void |
| `status` | [`string(Status113Enum)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/enumerations/status-113.md) | Required | Current status of the Volume | getStatus(): string | setStatus(string status): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\Volume1Builder;
use HetznerCloudAPILib\Models\Builders\Location16Builder;
use HetznerCloudAPILib\Models\Builders\ProtectionBuilder;
use HetznerCloudAPILib\Models\Status113Enum;

$volume1 = Volume1Builder::init(
    '2016-01-30T23:55:00+00:00',
    42,
    [
        'key0' => 'labels8'
    ],
    '/dev/disk/by-id/scsi-0HC_Volume_4711',
    Location16Builder::init(
        'Falkenstein',
        'DE',
        'Falkenstein DC Park 1',
        1,
        50.47612,
        12.370071,
        'fsn1',
        'eu-central'
    )->build(),
    'my-resource',
    ProtectionBuilder::init(
        false
    )->build(),
    42,
    Status113Enum::AVAILABLE
)
    ->format('xfs')
    ->server(12)
    ->build();
```



