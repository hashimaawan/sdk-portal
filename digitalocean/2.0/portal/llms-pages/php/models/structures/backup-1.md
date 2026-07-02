# Backup 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkJhY2t1cDE

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Backup1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `id` | `int` | Required | The unique identifier for the snapshot or backup. | getId(): int | setId(int id): void |
| `createdAt` | `DateTime` | Required | A time value given in ISO8601 combined date and time format that represents when the snapshot was created. | getCreatedAt(): \DateTime | setCreatedAt(\DateTime createdAt): void |
| `minDiskSize` | `int` | Required | The minimum size in GB required for a volume or Droplet to use this snapshot. | getMinDiskSize(): int | setMinDiskSize(int minDiskSize): void |
| `name` | `string` | Required | A human-readable name for the snapshot. | getName(): string | setName(string name): void |
| `regions` | `string[]` | Required | An array of the regions that the snapshot is available in. The regions are represented by their identifying slug values. | getRegions(): array | setRegions(array regions): void |
| `sizeGigabytes` | `float` | Required | The billable size of the snapshot in gigabytes. | getSizeGigabytes(): float | setSizeGigabytes(float sizeGigabytes): void |
| `type` | [`string(Type13)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/type-13.md) | Required | Describes the kind of image. It may be one of `snapshot` or `backup`. This specifies whether an image is a user-generated Droplet snapshot or automatically created Droplet backup. | getType(): string | setType(string type): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\Backup1Builder;
use DigitalOceanApiLib\Utils\DateTimeHelper;
use DigitalOceanApiLib\Models\Type13;
use DigitalOceanApiLib\ApiHelper;

$backup1 = Backup1Builder::init(
    6372321,
    DateTimeHelper::fromRfc3339DateTimeRequired('2020-07-28T16:47:44Z'),
    25,
    'web-01-1595954862243',
    [
        'nyc3',
        'sfo3'
    ],
    2.34,
    Type13::SNAPSHOT
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



