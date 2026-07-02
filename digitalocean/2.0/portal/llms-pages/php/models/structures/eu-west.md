# Eu West

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkV1V2VzdA

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`EuWest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `status` | [`?string(Status16)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/status-16.md) | Optional | - | getStatus(): ?string | setStatus(?string status): void |
| `statusChangedAt` | `?string` | Optional | - | getStatusChangedAt(): ?string | setStatusChangedAt(?string statusChangedAt): void |
| `thirtyDayUptimePercentage` | `?float` | Optional | - | getThirtyDayUptimePercentage(): ?float | setThirtyDayUptimePercentage(?float thirtyDayUptimePercentage): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\EuWestBuilder;
use DigitalOceanApiLib\Models\Status16;
use DigitalOceanApiLib\ApiHelper;

$euWest = EuWestBuilder::init()
    ->status(Status16::UP)
    ->statusChangedAt('2022-03-17T22:28:51Z')
    ->thirtyDayUptimePercentage(97.99)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



