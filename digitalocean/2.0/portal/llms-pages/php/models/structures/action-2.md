# Action 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkFjdGlvbjI

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Action2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `completedAt` | `?DateTime` | Optional | A time value given in ISO8601 combined date and time format that represents when the action was completed. | getCompletedAt(): ?\DateTime | setCompletedAt(?\DateTime completedAt): void |
| `id` | `?int` | Optional | A unique numeric ID that can be used to identify and reference an action. | getId(): ?int | setId(?int id): void |
| `region` | [`?Region`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/region.md) | Optional | - | getRegion(): ?Region | setRegion(?Region region): void |
| `regionSlug` | `?string` | Optional | - | getRegionSlug(): ?string | setRegionSlug(?string regionSlug): void |
| `resourceId` | `?int` | Optional | A unique identifier for the resource that the action is associated with. | getResourceId(): ?int | setResourceId(?int resourceId): void |
| `resourceType` | `?string` | Optional | The type of resource that the action is associated with. | getResourceType(): ?string | setResourceType(?string resourceType): void |
| `startedAt` | `?DateTime` | Optional | A time value given in ISO8601 combined date and time format that represents when the action was initiated. | getStartedAt(): ?\DateTime | setStartedAt(?\DateTime startedAt): void |
| `status` | [`?string(Status1)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/status-1.md) | Optional | The current status of the action. This can be "in-progress", "completed", or "errored".<br><br>**Default**: `Status1::INPROGRESS` | getStatus(): ?string | setStatus(?string status): void |
| `type` | `?string` | Optional | This is the type of action that the object represents. For example, this could be "transfer" to represent the state of an image transfer action. | getType(): ?string | setType(?string type): void |
| `projectId` | `?string` | Optional | The UUID of the project to which the reserved IP currently belongs. | getProjectId(): ?string | setProjectId(?string projectId): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\Action2Builder;
use DigitalOceanApiLib\Utils\DateTimeHelper;
use DigitalOceanApiLib\Models\Builders\RegionBuilder;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Models\Status1;

$action2 = Action2Builder::init()
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
    ->regionSlug('region_slug8')
    ->resourceId(3164444)
    ->resourceType('droplet')
    ->startedAt(DateTimeHelper::fromRfc3339DateTime('2020-11-14T16:29:21Z'))
    ->status(Status1::COMPLETED)
    ->type('create')
    ->projectId('746c6152-2fa2-11ed-92d3-27aaa54e4988')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



