# Team

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlRlYW0

When authorized in a team context, includes information about the current team.

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Team`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `name` | `?string` | Optional | The name for the current team. | getName(): ?string | setName(?string name): void |
| `uuid` | `?string` | Optional | The unique universal identifier for the current team. | getUuid(): ?string | setUuid(?string uuid): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\TeamBuilder;
use DigitalOceanApiLib\ApiHelper;

$team = TeamBuilder::init()
    ->name('My Team')
    ->uuid('5df3e3004a17e242b7c20ca6c9fc25b701a47ece')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



