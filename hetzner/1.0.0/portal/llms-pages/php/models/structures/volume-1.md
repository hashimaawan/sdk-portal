# Volume 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlZvbHVtZTE

*This model accepts additional fields of type array.*


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
| `status` | [`string(Status113)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/enumerations/status-113.md) | Required | Current status of the Volume | getStatus(): string | setStatus(string status): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\Volume1Builder;
use HetznerCloudApiLib\Models\Builders\Location16Builder;
use HetznerCloudApiLib\ApiHelper;
use HetznerCloudApiLib\Models\Builders\ProtectionBuilder;
use HetznerCloudApiLib\Models\Status113;

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
    )
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build(),
    'my-resource',
    ProtectionBuilder::init(
        false
    )
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build(),
    42,
    Status113::AVAILABLE
)
    ->format('xfs')
    ->server(12)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



