# Servers Metrics Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyME1ldHJpY3MlMjUyMFJlc3BvbnNl


# Class Name

`ServersMetricsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `metrics` | [`Metrics`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/metrics.md) | Required | - | getMetrics(): Metrics | setMetrics(Metrics metrics): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\ServersMetricsResponseBuilder;
use HetznerCloudAPILib\Models\Builders\MetricsBuilder;
use HetznerCloudAPILib\Models\Builders\TimeSeriesBuilder;

$serversMetricsResponse = ServersMetricsResponseBuilder::init(
    MetricsBuilder::init(
        '2017-01-01T23:00:00+00:00',
        '2017-01-01T00:00:00+00:00',
        60,
        [
            'name_of_timeseries' => TimeSeriesBuilder::init(
                [
                    [
                        1435781470.622,
                        '42'
                    ],
                    [
                        1435781471.622,
                        '43'
                    ]
                ]
            )->build()
        ]
    )->build()
)->build();
```



