# Statistics 3

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlN0YXRpc3RpY3Mz

*This model accepts additional fields of type array.*


# Class Name

`Statistics3`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `dpuExecutionInMillis` | `?int` | Optional | - | getDpuExecutionInMillis(): ?int | setDpuExecutionInMillis(?int dpuExecutionInMillis): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\Statistics3Builder;
use AmazonAthenaLib\ApiHelper;

$statistics3 = Statistics3Builder::init()
    ->dpuExecutionInMillis(130)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



