# Get Calculation Execution Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkdldENhbGN1bGF0aW9uRXhlY3V0aW9uUmVzcG9uc2U


# Class Name

`GetCalculationExecutionResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `calculationExecutionId` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36` | getCalculationExecutionId(): ?string | setCalculationExecutionId(?string calculationExecutionId): void |
| `sessionId` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | getSessionId(): ?string | setSessionId(?string sessionId): void |
| `description` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | getDescription(): ?string | setDescription(?string description): void |
| `workingDirectory` | `?string` | Optional | **Constraints**: *Maximum Length*: `1024`, *Pattern*: `^(https\|s3\|S3)://([^/]+)/?(.*)$` | getWorkingDirectory(): ?string | setWorkingDirectory(?string workingDirectory): void |
| `status` | [`?Status1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/status-1.md) | Optional | - | getStatus(): ?Status1 | setStatus(?Status1 status): void |
| `statistics` | [`?Statistics1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/statistics-1.md) | Optional | - | getStatistics(): ?Statistics1 | setStatistics(?Statistics1 statistics): void |
| `result` | [`?Result`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/result.md) | Optional | - | getResult(): ?Result | setResult(?Result result): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\GetCalculationExecutionResponseBuilder;
use AmazonAthenaLib\Models\Builders\Status1Builder;
use AmazonAthenaLib\Utils\DateTimeHelper;
use AmazonAthenaLib\Models\CalculationExecutionState1Enum;

$getCalculationExecutionResponse = GetCalculationExecutionResponseBuilder::init()
    ->calculationExecutionId('CalculationExecutionId4')
    ->sessionId('SessionId8')
    ->description('Description6')
    ->workingDirectory('WorkingDirectory8')
    ->status(
        Status1Builder::init()
            ->submissionDateTime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
            ->completionDateTime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
            ->state(CalculationExecutionState1Enum::CANCELING)
            ->stateChangeReason('StateChangeReason8')
            ->build()
    )
    ->build();
```



