# List Calculation Executions Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkxpc3RDYWxjdWxhdGlvbkV4ZWN1dGlvbnNSZXNwb25zZQ

*This model accepts additional fields of type array.*


# Class Name

`ListCalculationExecutionsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `nextToken` | `?string` | Optional | **Constraints**: *Maximum Length*: `2048` | getNextToken(): ?string | setNextToken(?string nextToken): void |
| `calculations` | [`?(CalculationSummary[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/calculation-summary.md) | Optional | **Constraints**: *Minimum Items*: `0`, *Maximum Items*: `100` | getCalculations(): ?array | setCalculations(?array calculations): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\ListCalculationExecutionsResponseBuilder;
use AmazonAthenaLib\Models\Builders\CalculationSummaryBuilder;
use AmazonAthenaLib\Models\Builders\Status1Builder;
use AmazonAthenaLib\Utils\DateTimeHelper;
use AmazonAthenaLib\Models\CalculationExecutionState1;
use AmazonAthenaLib\ApiHelper;

$listCalculationExecutionsResponse = ListCalculationExecutionsResponseBuilder::init()
    ->nextToken('NextToken8')
    ->calculations(
        [
            CalculationSummaryBuilder::init()
                ->calculationExecutionId('CalculationExecutionId0')
                ->description('Description2')
                ->status(
                    Status1Builder::init()
                        ->submissionDateTime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                        ->completionDateTime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                        ->state(CalculationExecutionState1::CANCELING)
                        ->stateChangeReason('StateChangeReason8')
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                )
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



