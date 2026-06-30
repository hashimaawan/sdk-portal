# Placement Group Nullable

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRlBsYWNlbWVudEdyb3VwTnVsbGFibGU


# Class Name

`PlacementGroupNullable`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `created` | `string` | Required | Point in time when the Resource was created (in ISO-8601 format) | getCreated(): string | setCreated(string created): void |
| `id` | `int` | Required | ID of the Resource | getId(): int | setId(int id): void |
| `labels` | `array<string,string>` | Required | User-defined labels (key-value pairs) | getLabels(): array | setLabels(array labels): void |
| `name` | `string` | Required | Name of the Resource. Must be unique per Project. | getName(): string | setName(string name): void |
| `servers` | `int[]` | Required | Array of IDs of Servers that are part of this Placement Group | getServers(): array | setServers(array servers): void |
| `type` | `string` | Required, Constant | Type of the Placement Group<br><br>**Value**: `'spread'` | getType(): string | setType(string type): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\PlacementGroupNullableBuilder;

$placementGroupNullable = PlacementGroupNullableBuilder::init(
    '2016-01-30T23:55:00+00:00',
    42,
    [
        'key0' => 'labels2'
    ],
    'my-resource',
    [
        42
    ]
)->build();
```



