# Stop Calculation Execution Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlN0b3BDYWxjdWxhdGlvbkV4ZWN1dGlvblJlcXVlc3Q


# Class Name

`StopCalculationExecutionRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `calculationExecutionId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36` | getCalculationExecutionId(): string | setCalculationExecutionId(string calculationExecutionId): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\StopCalculationExecutionRequestBuilder;

$stopCalculationExecutionRequest = StopCalculationExecutionRequestBuilder::init(
    'CalculationExecutionId2'
)->build();
```



