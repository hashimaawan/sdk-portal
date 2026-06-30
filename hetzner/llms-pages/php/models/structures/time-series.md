# Time Series

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRlRpbWVTZXJpZXM


# Class Name

`TimeSeries`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `values` | array<array<float\|string>> | Required | This is 2d Array of a container for one-of cases. | getValues(): array | setValues(array values): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\TimeSeriesBuilder;

$timeSeries = TimeSeriesBuilder::init(
    [
        [
            138.94,
            138.95
        ],
        [
            138.94,
            138.95
        ]
    ]
)->build();
```



