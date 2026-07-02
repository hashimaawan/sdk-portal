# Session Statistics

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlNlc3Npb25TdGF0aXN0aWNz

Contains statistics for a session.

*This model accepts additional fields of type array.*


# Class Name

`SessionStatistics`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `dpuExecutionInMillis` | `?int` | Optional | - | getDpuExecutionInMillis(): ?int | setDpuExecutionInMillis(?int dpuExecutionInMillis): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\SessionStatisticsBuilder;
use AmazonAthenaLib\ApiHelper;

$sessionStatistics = SessionStatisticsBuilder::init()
    ->dpuExecutionInMillis(188)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



