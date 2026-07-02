# Calculation Summary

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkNhbGN1bGF0aW9uU3VtbWFyeQ

Summary information for a notebook calculation.

*This model accepts additional fields of type array.*


# Class Name

`CalculationSummary`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `calculationExecutionId` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36` | getCalculationExecutionId(): ?string | setCalculationExecutionId(?string calculationExecutionId): void |
| `description` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | getDescription(): ?string | setDescription(?string description): void |
| `status` | [`?Status1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/status-1.md) | Optional | - | getStatus(): ?Status1 | setStatus(?Status1 status): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\CalculationSummaryBuilder;
use AmazonAthenaLib\Models\Builders\Status1Builder;
use AmazonAthenaLib\Utils\DateTimeHelper;
use AmazonAthenaLib\Models\CalculationExecutionState1;
use AmazonAthenaLib\ApiHelper;

$calculationSummary = CalculationSummaryBuilder::init()
    ->calculationExecutionId('CalculationExecutionId4')
    ->description('Description6')
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
    ->build();
```



