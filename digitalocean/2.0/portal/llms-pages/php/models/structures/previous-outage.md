# Previous Outage

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlByZXZpb3VzT3V0YWdl

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`PreviousOutage`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `durationSeconds` | `?int` | Optional | - | getDurationSeconds(): ?int | setDurationSeconds(?int durationSeconds): void |
| `endedAt` | `?string` | Optional | - | getEndedAt(): ?string | setEndedAt(?string endedAt): void |
| `region` | `?string` | Optional | - | getRegion(): ?string | setRegion(?string region): void |
| `startedAt` | `?string` | Optional | - | getStartedAt(): ?string | setStartedAt(?string startedAt): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\PreviousOutageBuilder;
use DigitalOceanApiLib\ApiHelper;

$previousOutage = PreviousOutageBuilder::init()
    ->durationSeconds(120)
    ->endedAt('2022-03-17T18:06:55Z')
    ->region('us_east')
    ->startedAt('2022-03-17T18:04:55Z')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



