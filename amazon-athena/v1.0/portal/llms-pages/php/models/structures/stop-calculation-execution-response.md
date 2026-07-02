# Stop Calculation Execution Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlN0b3BDYWxjdWxhdGlvbkV4ZWN1dGlvblJlc3BvbnNl

*This model accepts additional fields of type array.*


# Class Name

`StopCalculationExecutionResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `state` | [`?string(CalculationExecutionState4)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/enumerations/calculation-execution-state-4.md) | Optional | - | getState(): ?string | setState(?string state): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\StopCalculationExecutionResponseBuilder;
use AmazonAthenaLib\Models\CalculationExecutionState4;
use AmazonAthenaLib\ApiHelper;

$stopCalculationExecutionResponse = StopCalculationExecutionResponseBuilder::init()
    ->state(CalculationExecutionState4::QUEUED)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



