# V2 Apps Metrics Bandwidth Daily Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBNZXRyaWNzJTI1MjBCYW5kd2lkdGglMjUyMERhaWx5JTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2AppsMetricsBandwidthDailyResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `appBandwidthUsage` | [`?(AppBandwidthUsage[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/app-bandwidth-usage.md) | Optional | A list of bandwidth usage details by app. | getAppBandwidthUsage(): ?array | setAppBandwidthUsage(?array appBandwidthUsage): void |
| `date` | `?DateTime` | Optional | The date for the metrics data. | getDate(): ?\DateTime | setDate(?\DateTime date): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2AppsMetricsBandwidthDailyResponseBuilder;
use DigitalOceanApiLib\Models\Builders\AppBandwidthUsageBuilder;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Utils\DateTimeHelper;

$v2AppsMetricsBandwidthDailyResponse = V2AppsMetricsBandwidthDailyResponseBuilder::init()
    ->appBandwidthUsage(
        [
            AppBandwidthUsageBuilder::init()
                ->appId('app_id4')
                ->bandwidthBytes('bandwidth_bytes6')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            AppBandwidthUsageBuilder::init()
                ->appId('app_id4')
                ->bandwidthBytes('bandwidth_bytes6')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->date(DateTimeHelper::fromRfc3339DateTime('2023-01-17T00:00:00Z'))
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



