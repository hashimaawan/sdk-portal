# Status

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlN0YXR1cw

*This model accepts additional fields of type array.*


# Class Name

`Status`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `state` | [`?string(QueryExecutionState1)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/enumerations/query-execution-state-1.md) | Optional | - | getState(): ?string | setState(?string state): void |
| `stateChangeReason` | `?string` | Optional | - | getStateChangeReason(): ?string | setStateChangeReason(?string stateChangeReason): void |
| `submissionDateTime` | `?DateTime` | Optional | - | getSubmissionDateTime(): ?\DateTime | setSubmissionDateTime(?\DateTime submissionDateTime): void |
| `completionDateTime` | `?DateTime` | Optional | - | getCompletionDateTime(): ?\DateTime | setCompletionDateTime(?\DateTime completionDateTime): void |
| `athenaError` | [`?AthenaError2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/athena-error-2.md) | Optional | - | getAthenaError(): ?AthenaError2 | setAthenaError(?AthenaError2 athenaError): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\StatusBuilder;
use AmazonAthenaLib\Models\QueryExecutionState1;
use AmazonAthenaLib\Utils\DateTimeHelper;
use AmazonAthenaLib\Models\Builders\AthenaError2Builder;
use AmazonAthenaLib\ApiHelper;

$status = StatusBuilder::init()
    ->state(QueryExecutionState1::QUEUED)
    ->stateChangeReason('StateChangeReason8')
    ->submissionDateTime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
    ->completionDateTime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
    ->athenaError(
        AthenaError2Builder::init()
            ->errorCategory(3)
            ->errorType(128)
            ->retryable(false)
            ->errorMessage('ErrorMessage8')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



