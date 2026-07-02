# Scheduled Runs

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlNjaGVkdWxlZFJ1bnM

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`ScheduledRuns`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `lastRunAt` | `?string` | Optional | Indicates last run time. null value indicates trigger not run yet. | getLastRunAt(): ?string | setLastRunAt(?string lastRunAt): void |
| `nextRunAt` | `?string` | Optional | Indicates next run time. null value indicates trigger will not run. | getNextRunAt(): ?string | setNextRunAt(?string nextRunAt): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\ScheduledRunsBuilder;
use DigitalOceanApiLib\ApiHelper;

$scheduledRuns = ScheduledRunsBuilder::init()
    ->lastRunAt('2022-11-11T04:16:45Z')
    ->nextRunAt('2022-11-11T04:16:45Z')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



