# Stop Calculation Execution Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlN0b3BDYWxjdWxhdGlvbkV4ZWN1dGlvblJlc3BvbnNl


# Class Name

`StopCalculationExecutionResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `state` | [`?string(CalculationExecutionState4Enum)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/enumerations/calculation-execution-state-4.md) | Optional | - | getState(): ?string | setState(?string state): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\StopCalculationExecutionResponseBuilder;
use AmazonAthenaLib\Models\CalculationExecutionState4Enum;

$stopCalculationExecutionResponse = StopCalculationExecutionResponseBuilder::init()
    ->state(CalculationExecutionState4Enum::QUEUED)
    ->build();
```



