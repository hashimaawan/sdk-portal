# Time Series

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlRpbWVTZXJpZXM

*This model accepts additional fields of type array.*


# Class Name

`TimeSeries`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `values` | array<array<float\|string>> | Required | This is 2d Array of a container for one-of cases. | getValues(): array | setValues(array values): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\TimeSeriesBuilder;
use HetznerCloudApiLib\ApiHelper;

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
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



