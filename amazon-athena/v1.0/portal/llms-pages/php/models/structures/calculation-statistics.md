# Calculation Statistics

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkNhbGN1bGF0aW9uU3RhdGlzdGljcw

Contains statistics for a notebook calculation.

*This model accepts additional fields of type array.*


# Class Name

`CalculationStatistics`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `dpuExecutionInMillis` | `?int` | Optional | - | getDpuExecutionInMillis(): ?int | setDpuExecutionInMillis(?int dpuExecutionInMillis): void |
| `progress` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | getProgress(): ?string | setProgress(?string progress): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\CalculationStatisticsBuilder;
use AmazonAthenaLib\ApiHelper;

$calculationStatistics = CalculationStatisticsBuilder::init()
    ->dpuExecutionInMillis(248)
    ->progress('Progress8')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



