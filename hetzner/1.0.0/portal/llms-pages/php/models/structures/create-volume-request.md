# Create Volume Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkNyZWF0ZVZvbHVtZVJlcXVlc3Q

*This model accepts additional fields of type array.*


# Class Name

`CreateVolumeRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `automount` | `?bool` | Optional | Auto-mount Volume after attach. `server` must be provided. | getAutomount(): ?bool | setAutomount(?bool automount): void |
| `format` | `?string` | Optional | Format Volume after creation. One of: `xfs`, `ext4` | getFormat(): ?string | setFormat(?string format): void |
| `labels` | `?array` | Optional | User-defined labels (key-value pairs) | getLabels(): ?array | setLabels(?array labels): void |
| `location` | `?string` | Optional | Location to create the Volume in (can be omitted if Server is specified) | getLocation(): ?string | setLocation(?string location): void |
| `name` | `string` | Required | Name of the volume | getName(): string | setName(string name): void |
| `server` | `?int` | Optional | Server to which to attach the Volume once it's created (Volume will be created in the same Location as the server) | getServer(): ?int | setServer(?int server): void |
| `size` | `int` | Required | Size of the Volume in GB | getSize(): int | setSize(int size): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\CreateVolumeRequestBuilder;
use HetznerCloudApiLib\ApiHelper;

$createVolumeRequest = CreateVolumeRequestBuilder::init(
    'databases-storage',
    42
)
    ->automount(false)
    ->format('xfs')
    ->labels(ApiHelper::deserialize('{"labelkey":"value"}'))
    ->location('nbg1')
    ->server(182)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



