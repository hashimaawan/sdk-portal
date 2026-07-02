# Snapshot

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlNuYXBzaG90

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Snapshot`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `id` | `string` | Required | The unique identifier for the snapshot. | getId(): string | setId(string id): void |
| `createdAt` | `DateTime` | Required | A time value given in ISO8601 combined date and time format that represents when the snapshot was created. | getCreatedAt(): \DateTime | setCreatedAt(\DateTime createdAt): void |
| `minDiskSize` | `int` | Required | The minimum size in GB required for a volume or Droplet to use this snapshot. | getMinDiskSize(): int | setMinDiskSize(int minDiskSize): void |
| `name` | `string` | Required | A human-readable name for the snapshot. | getName(): string | setName(string name): void |
| `regions` | `string[]` | Required | An array of the regions that the snapshot is available in. The regions are represented by their identifying slug values. | getRegions(): array | setRegions(array regions): void |
| `sizeGigabytes` | `float` | Required | The billable size of the snapshot in gigabytes. | getSizeGigabytes(): float | setSizeGigabytes(float sizeGigabytes): void |
| `resourceId` | `string` | Required | The unique identifier for the resource that the snapshot originated from. | getResourceId(): string | setResourceId(string resourceId): void |
| `resourceType` | [`string(ResourceType1)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/resource-type-1.md) | Required | The type of resource that the snapshot originated from. | getResourceType(): string | setResourceType(string resourceType): void |
| `tags` | `?(string[])` | Required | An array of Tags the snapshot has been tagged with. | getTags(): ?array | setTags(?array tags): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\SnapshotBuilder;
use DigitalOceanApiLib\Utils\DateTimeHelper;
use DigitalOceanApiLib\Models\ResourceType1;
use DigitalOceanApiLib\ApiHelper;

$snapshot = SnapshotBuilder::init(
    '6372321',
    DateTimeHelper::fromRfc3339DateTimeRequired('2020-07-28T16:47:44Z'),
    25,
    'web-01-1595954862243',
    [
        'nyc3',
        'sfo3'
    ],
    2.34,
    '200776916',
    ResourceType1::DROPLET
)
    ->tags(
        [
            'web',
            'env:prod'
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



