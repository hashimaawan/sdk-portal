# Get Calculation Execution Status Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkdldENhbGN1bGF0aW9uRXhlY3V0aW9uU3RhdHVzUmVzcG9uc2U

*This model accepts additional fields of type array.*


# Class Name

`GetCalculationExecutionStatusResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `status` | [`?Status1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/status-1.md) | Optional | - | getStatus(): ?Status1 | setStatus(?Status1 status): void |
| `statistics` | [`?Statistics1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/statistics-1.md) | Optional | - | getStatistics(): ?Statistics1 | setStatistics(?Statistics1 statistics): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\GetCalculationExecutionStatusResponseBuilder;
use AmazonAthenaLib\Models\Builders\Status1Builder;
use AmazonAthenaLib\Utils\DateTimeHelper;
use AmazonAthenaLib\Models\CalculationExecutionState1;
use AmazonAthenaLib\ApiHelper;
use AmazonAthenaLib\Models\Builders\Statistics1Builder;

$getCalculationExecutionStatusResponse = GetCalculationExecutionStatusResponseBuilder::init()
    ->status(
        Status1Builder::init()
            ->submissionDateTime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
            ->completionDateTime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
            ->state(CalculationExecutionState1::CANCELING)
            ->stateChangeReason('StateChangeReason8')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->statistics(
        Statistics1Builder::init()
            ->dpuExecutionInMillis(164)
            ->progress('Progress6')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



