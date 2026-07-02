# Maintenance Policy

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRk1haW50ZW5hbmNlUG9saWN5

An object specifying the maintenance window policy for the Kubernetes cluster.

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`MaintenancePolicy`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `day` | [`?string(Day)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/day.md) | Optional | The day of the maintenance window policy. May be one of `monday` through `sunday`, or `any` to indicate an arbitrary week day. | getDay(): ?string | setDay(?string day): void |
| `duration` | `?string` | Optional, Read-only | The duration of the maintenance window policy in human-readable format. | getDuration(): ?string | setDuration(?string duration): void |
| `startTime` | `?string` | Optional | The start time in UTC of the maintenance window policy in 24-hour clock format / HH:MM notation (e.g., `15:00`). | getStartTime(): ?string | setStartTime(?string startTime): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\MaintenancePolicyBuilder;
use DigitalOceanApiLib\Models\Day;
use DigitalOceanApiLib\ApiHelper;

$maintenancePolicy = MaintenancePolicyBuilder::init()
    ->day(Day::ANY)
    ->duration('4h0m0s')
    ->startTime('12:00')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



