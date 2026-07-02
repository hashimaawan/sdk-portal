# Action 4

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkFjdGlvbjQ

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Action4`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `resourceId` | `?int` | Optional | A unique identifier for the resource that the action is associated with. | getResourceId(): ?int | setResourceId(?int resourceId): void |
| `type` | `?string` | Optional | This is the type of action that the object represents. For example, this could be "attach_volume" to represent the state of a volume attach action. | getType(): ?string | setType(?string type): void |
| `completedAt` | `?DateTime` | Optional | A time value given in ISO8601 combined date and time format that represents when the action was completed. | getCompletedAt(): ?\DateTime | setCompletedAt(?\DateTime completedAt): void |
| `id` | `?int` | Optional | A unique numeric ID that can be used to identify and reference an action. | getId(): ?int | setId(?int id): void |
| `region` | [`?Region`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/region.md) | Optional | - | getRegion(): ?Region | setRegion(?Region region): void |
| `regionSlug` | `?string` | Optional | - | getRegionSlug(): ?string | setRegionSlug(?string regionSlug): void |
| `resourceType` | `?string` | Optional | The type of resource that the action is associated with. | getResourceType(): ?string | setResourceType(?string resourceType): void |
| `startedAt` | `?DateTime` | Optional | A time value given in ISO8601 combined date and time format that represents when the action was initiated. | getStartedAt(): ?\DateTime | setStartedAt(?\DateTime startedAt): void |
| `status` | [`?string(Status1)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/status-1.md) | Optional | The current status of the action. This can be "in-progress", "completed", or "errored".<br><br>**Default**: `Status1::INPROGRESS` | getStatus(): ?string | setStatus(?string status): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\Action4Builder;
use DigitalOceanApiLib\Utils\DateTimeHelper;
use DigitalOceanApiLib\Models\Builders\RegionBuilder;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Models\Status1;

$action4 = Action4Builder::init()
    ->resourceId(160)
    ->type('attach_volume')
    ->completedAt(DateTimeHelper::fromRfc3339DateTime('2020-11-14T16:30:06Z'))
    ->id(36804636)
    ->region(
        RegionBuilder::init(
            false,
            [
                'features7',
                'features8',
                'features9'
            ],
            'name6',
            [
                'sizes6'
            ],
            'slug0'
        )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->resourceType('droplet')
    ->startedAt(DateTimeHelper::fromRfc3339DateTime('2020-11-14T16:29:21Z'))
    ->status(Status1::COMPLETED)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



