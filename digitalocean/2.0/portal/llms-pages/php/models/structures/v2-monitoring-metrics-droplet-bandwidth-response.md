# V2 Monitoring Metrics Droplet Bandwidth Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBNb25pdG9yaW5nJTI1MjBNZXRyaWNzJTI1MjBEcm9wbGV0JTI1MjBCYW5kd2lkdGglMjUyMFJlc3BvbnNl

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2MonitoringMetricsDropletBandwidthResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `data` | [`Data`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/data.md) | Required | - | getData(): Data | setData(Data data): void |
| `status` | [`string(Status13)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/status-13.md) | Required | - | getStatus(): string | setStatus(string status): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2MonitoringMetricsDropletBandwidthResponseBuilder;
use DigitalOceanApiLib\Models\Builders\DataBuilder;
use DigitalOceanApiLib\Models\Builders\ResultBuilder;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Models\Status13;

$v2MonitoringMetricsDropletBandwidthResponse = V2MonitoringMetricsDropletBandwidthResponseBuilder::init(
    DataBuilder::init(
        [
            ResultBuilder::init(
                [
                    'host_id' => '19201920'
                ],
                [
                    [
                        1435781430,
                        '1'
                    ],
                    [
                        1435781445,
                        '1'
                    ]
                ]
            )
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build(),
    Status13::SUCCESS
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



