# Statistics 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlN0YXRpc3RpY3Mx

*This model accepts additional fields of type array.*


# Class Name

`Statistics1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `dpuExecutionInMillis` | `?int` | Optional | - | getDpuExecutionInMillis(): ?int | setDpuExecutionInMillis(?int dpuExecutionInMillis): void |
| `progress` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | getProgress(): ?string | setProgress(?string progress): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\Statistics1Builder;
use AmazonAthenaLib\ApiHelper;

$statistics1 = Statistics1Builder::init()
    ->dpuExecutionInMillis(148)
    ->progress('Progress4')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



