# Metrics

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRk1ldHJpY3M


# Class Name

`Metrics`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `end` | `string` | Required | End of period of metrics reported (in ISO-8601 format) | getEnd(): string | setEnd(string end): void |
| `start` | `string` | Required | Start of period of metrics reported (in ISO-8601 format) | getStart(): string | setStart(string start): void |
| `step` | `float` | Required | Resolution of results in seconds. | getStep(): float | setStep(float step): void |
| `timeSeries` | [`array<string,TimeSeries>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/time-series.md) | Required | Hash with timeseries information, containing the name of timeseries as key | getTimeSeries(): array | setTimeSeries(array timeSeries): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\MetricsBuilder;
use HetznerCloudAPILib\Models\Builders\TimeSeriesBuilder;

$metrics = MetricsBuilder::init(
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
)->build();
```



