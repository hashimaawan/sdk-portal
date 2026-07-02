# Executors Summary

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkV4ZWN1dG9yc1N1bW1hcnk

Contains summary information about an executor.

*This model accepts additional fields of type array.*


# Class Name

`ExecutorsSummary`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `executorId` | `string` | Required | **Constraints**: *Maximum Length*: `100000`, *Pattern*: `.*` | getExecutorId(): string | setExecutorId(string executorId): void |
| `executorType` | [`?string(ExecutorType2)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/enumerations/executor-type-2.md) | Optional | - | getExecutorType(): ?string | setExecutorType(?string executorType): void |
| `startDateTime` | `?int` | Optional | - | getStartDateTime(): ?int | setStartDateTime(?int startDateTime): void |
| `terminationDateTime` | `?int` | Optional | - | getTerminationDateTime(): ?int | setTerminationDateTime(?int terminationDateTime): void |
| `executorState` | [`?string(ExecutorState3)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/enumerations/executor-state-3.md) | Optional | - | getExecutorState(): ?string | setExecutorState(?string executorState): void |
| `executorSize` | `?int` | Optional | - | getExecutorSize(): ?int | setExecutorSize(?int executorSize): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\ExecutorsSummaryBuilder;
use AmazonAthenaLib\Models\ExecutorType2;
use AmazonAthenaLib\Models\ExecutorState3;
use AmazonAthenaLib\ApiHelper;

$executorsSummary = ExecutorsSummaryBuilder::init(
    'ExecutorId8'
)
    ->executorType(ExecutorType2::WORKER)
    ->startDateTime(52)
    ->terminationDateTime(56)
    ->executorState(ExecutorState3::CREATING)
    ->executorSize(222)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



