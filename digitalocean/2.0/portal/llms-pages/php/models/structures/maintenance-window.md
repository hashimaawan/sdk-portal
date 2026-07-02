# Maintenance Window

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRk1haW50ZW5hbmNlV2luZG93

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`MaintenanceWindow`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `day` | `string` | Required | The day of the week on which to apply maintenance updates. | getDay(): string | setDay(string day): void |
| `description` | `?(string[])` | Optional, Read-only | A list of strings, each containing information about a pending maintenance update. | getDescription(): ?array | setDescription(?array description): void |
| `hour` | `string` | Required | The hour in UTC at which maintenance updates will be applied in 24 hour format. | getHour(): string | setHour(string hour): void |
| `pending` | `?bool` | Optional, Read-only | A boolean value indicating whether any maintenance is scheduled to be performed in the next window. | getPending(): ?bool | setPending(?bool pending): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\MaintenanceWindowBuilder;
use DigitalOceanApiLib\ApiHelper;

$maintenanceWindow = MaintenanceWindowBuilder::init(
    'tuesday',
    '14:00'
)
    ->description(
        [
            'Update TimescaleDB to version 1.2.1',
            'Upgrade to PostgreSQL 11.2 and 10.7 bugfix releases'
        ]
    )
    ->pending(true)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



