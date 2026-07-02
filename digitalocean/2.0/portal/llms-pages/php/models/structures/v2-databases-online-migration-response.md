# V2 Databases Online Migration Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyME9ubGluZSUyNTIwTWlncmF0aW9uJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2DatabasesOnlineMigrationResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `createdAt` | `?string` | Optional | The time the migration was initiated, in ISO 8601 format. | getCreatedAt(): ?string | setCreatedAt(?string createdAt): void |
| `id` | `?string` | Optional | The ID of the most recent migration. | getId(): ?string | setId(?string id): void |
| `status` | [`?string(Status5)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/status-5.md) | Optional | The current status of the migration. | getStatus(): ?string | setStatus(?string status): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2DatabasesOnlineMigrationResponseBuilder;
use DigitalOceanApiLib\Models\Status5;
use DigitalOceanApiLib\ApiHelper;

$v2DatabasesOnlineMigrationResponse = V2DatabasesOnlineMigrationResponseBuilder::init()
    ->createdAt('2020-10-29T15:57:38Z')
    ->id('77b28fc8-19ff-11eb-8c9c-c68e24557488')
    ->status(Status5::RUNNING)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



