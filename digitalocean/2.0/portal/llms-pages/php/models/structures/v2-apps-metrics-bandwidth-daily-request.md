# V2 Apps Metrics Bandwidth Daily Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBNZXRyaWNzJTI1MjBCYW5kd2lkdGglMjUyMERhaWx5JTI1MjBSZXF1ZXN0

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2AppsMetricsBandwidthDailyRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `appIds` | `string[]` | Required | A list of app IDs to query bandwidth metrics for.<br><br>**Constraints**: *Maximum Items*: `100` | getAppIds(): array | setAppIds(array appIds): void |
| `date` | `?DateTime` | Optional | Optional day to query. Only the date component of the timestamp will be considered. Default: yesterday. | getDate(): ?\DateTime | setDate(?\DateTime date): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2AppsMetricsBandwidthDailyRequestBuilder;
use DigitalOceanApiLib\Utils\DateTimeHelper;
use DigitalOceanApiLib\ApiHelper;

$v2AppsMetricsBandwidthDailyRequest = V2AppsMetricsBandwidthDailyRequestBuilder::init(
    [
        '4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf',
        'c2a93513-8d9b-4223-9d61-5e7272c81cf5'
    ]
)
    ->date(DateTimeHelper::fromRfc3339DateTime('2023-01-17T00:00:00Z'))
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



