# Executors Summary

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkV4ZWN1dG9yc1N1bW1hcnk

Contains summary information about an executor.


# Class Name

`ExecutorsSummary`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `executorId` | `string` | Required | **Constraints**: *Maximum Length*: `100000`, *Pattern*: `.*` | getExecutorId(): string | setExecutorId(string executorId): void |
| `executorType` | [`?string(ExecutorType2Enum)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/enumerations/executor-type-2.md) | Optional | - | getExecutorType(): ?string | setExecutorType(?string executorType): void |
| `startDateTime` | `?int` | Optional | - | getStartDateTime(): ?int | setStartDateTime(?int startDateTime): void |
| `terminationDateTime` | `?int` | Optional | - | getTerminationDateTime(): ?int | setTerminationDateTime(?int terminationDateTime): void |
| `executorState` | [`?string(ExecutorState3Enum)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/enumerations/executor-state-3.md) | Optional | - | getExecutorState(): ?string | setExecutorState(?string executorState): void |
| `executorSize` | `?int` | Optional | - | getExecutorSize(): ?int | setExecutorSize(?int executorSize): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\ExecutorsSummaryBuilder;
use AmazonAthenaLib\Models\ExecutorType2Enum;
use AmazonAthenaLib\Models\ExecutorState3Enum;

$executorsSummary = ExecutorsSummaryBuilder::init(
    'ExecutorId8'
)
    ->executorType(ExecutorType2Enum::WORKER)
    ->startDateTime(52)
    ->terminationDateTime(56)
    ->executorState(ExecutorState3Enum::CREATING)
    ->executorSize(222)
    ->build();
```



