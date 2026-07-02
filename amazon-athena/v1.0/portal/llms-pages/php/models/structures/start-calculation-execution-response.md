# Start Calculation Execution Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlN0YXJ0Q2FsY3VsYXRpb25FeGVjdXRpb25SZXNwb25zZQ

*This model accepts additional fields of type array.*


# Class Name

`StartCalculationExecutionResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `calculationExecutionId` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36` | getCalculationExecutionId(): ?string | setCalculationExecutionId(?string calculationExecutionId): void |
| `state` | [`?string(CalculationExecutionState4)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/enumerations/calculation-execution-state-4.md) | Optional | - | getState(): ?string | setState(?string state): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\StartCalculationExecutionResponseBuilder;
use AmazonAthenaLib\Models\CalculationExecutionState4;
use AmazonAthenaLib\ApiHelper;

$startCalculationExecutionResponse = StartCalculationExecutionResponseBuilder::init()
    ->calculationExecutionId('CalculationExecutionId0')
    ->state(CalculationExecutionState4::CANCELING)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



