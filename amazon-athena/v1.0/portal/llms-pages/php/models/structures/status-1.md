# Status 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlN0YXR1czE


# Class Name

`Status1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `submissionDateTime` | `?DateTime` | Optional | - | getSubmissionDateTime(): ?\DateTime | setSubmissionDateTime(?\DateTime submissionDateTime): void |
| `completionDateTime` | `?DateTime` | Optional | - | getCompletionDateTime(): ?\DateTime | setCompletionDateTime(?\DateTime completionDateTime): void |
| `state` | [`?string(CalculationExecutionState1Enum)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/enumerations/calculation-execution-state-1.md) | Optional | - | getState(): ?string | setState(?string state): void |
| `stateChangeReason` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | getStateChangeReason(): ?string | setStateChangeReason(?string stateChangeReason): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\Status1Builder;
use AmazonAthenaLib\Utils\DateTimeHelper;
use AmazonAthenaLib\Models\CalculationExecutionState1Enum;

$status1 = Status1Builder::init()
    ->submissionDateTime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
    ->completionDateTime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
    ->state(CalculationExecutionState1Enum::QUEUED)
    ->stateChangeReason('StateChangeReason0')
    ->build();
```



