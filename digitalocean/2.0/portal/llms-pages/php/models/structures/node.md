# Node

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRk5vZGU

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Node`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `createdAt` | `?DateTime` | Optional | A time value given in ISO8601 combined date and time format that represents when the node was created. | getCreatedAt(): ?\DateTime | setCreatedAt(?\DateTime createdAt): void |
| `dropletId` | `?string` | Optional | The ID of the Droplet used for the worker node. | getDropletId(): ?string | setDropletId(?string dropletId): void |
| `id` | `?string` | Optional | A unique ID that can be used to identify and reference the node. | getId(): ?string | setId(?string id): void |
| `name` | `?string` | Optional | An automatically generated, human-readable name for the node. | getName(): ?string | setName(?string name): void |
| `status` | [`?Status10`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/status-10.md) | Optional | An object containing a `state` attribute whose value is set to a string indicating the current status of the node. | getStatus(): ?Status10 | setStatus(?Status10 status): void |
| `updatedAt` | `?DateTime` | Optional | A time value given in ISO8601 combined date and time format that represents when the node was last updated. | getUpdatedAt(): ?\DateTime | setUpdatedAt(?\DateTime updatedAt): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\NodeBuilder;
use DigitalOceanApiLib\Utils\DateTimeHelper;
use DigitalOceanApiLib\Models\Builders\Status10Builder;
use DigitalOceanApiLib\Models\State1;
use DigitalOceanApiLib\ApiHelper;

$node = NodeBuilder::init()
    ->createdAt(DateTimeHelper::fromRfc3339DateTime('2018-11-15T16:00:11Z'))
    ->dropletId('205545370')
    ->id('e78247f8-b1bb-4f7a-8db9-2a5f8d4b8f8f')
    ->name('adoring-newton-3niq')
    ->status(
        Status10Builder::init()
            ->state(State1::PROVISIONING)
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->updatedAt(DateTimeHelper::fromRfc3339DateTime('2018-11-15T16:00:11Z'))
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



