# Stop Calculation Execution Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlN0b3BDYWxjdWxhdGlvbkV4ZWN1dGlvblJlcXVlc3Q

*This model accepts additional fields of type array.*


# Class Name

`StopCalculationExecutionRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `calculationExecutionId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36` | getCalculationExecutionId(): string | setCalculationExecutionId(string calculationExecutionId): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\StopCalculationExecutionRequestBuilder;
use AmazonAthenaLib\ApiHelper;

$stopCalculationExecutionRequest = StopCalculationExecutionRequestBuilder::init(
    'CalculationExecutionId2'
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



